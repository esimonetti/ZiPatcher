Given two Sugar folders: current (most recent system) and backup (older version)


cd current


diff -auNwrq -x cache -x upload -x config.php -x config_override.php -x zh_CN -x uk_UA* -x tr_TR* -x sv_SE* -x sr_RS* -x sq_AL* -x sk_SK* -x ru_RU* -x ro_RO* -x pt_PT* -x pt_BR* -x pl_PL* -x nl_NL* -x nb_NO* -x lv_LV* -x ko_KR* -x ja_JP* -x it_it* -x hu_HU* -x he_IL* -x fr_FR* -x fi_FI* -x et_EE* -x es_LA* -x es_ES* -x en_UK* -x el_EL* -x de_DE* -x da_DK* -x cs_CZ* -x ca_ES* -x bg_BG* -x ar_SA* -x lt_LT* --ignore-matching-lines="// created: " --ignore-matching-lines="//created: " -x "*.php_1*" -x *.ext.php -x *blowfish* -x .gitignore -x .gitattributes -x .htaccess -x "*.DS_Store" -x vendor -x "*.log" -x "*.zip" -x "*.sql" -x "*.tgz" -x "*.md" -x "*.filepart" ../backup ./ | awk '{print $4}'


Now you have a full list of modified files to include on ZiPatcher
