CHANGELOG for Sulu Demo
=======================

* dev-master
    * FEATURE #51 [GENERAL] Updated to Sulu Version 1.6.0 RC1 and added SuluArticleBundle
        DEPLOY:
            bin/console doctrine:phpcr:nodes:update --query "SELECT * FROM [nt:base] AS n WHERE [i18n:en-author] IS NOT NULL AND ISDESCENDANTNODE(n, '/cmf')" --apply-closure="\$node->getProperty('i18n:en-author')->remove();"
            bin/console doctrine:phpcr:nodes:update --query "SELECT * FROM [nt:base] AS n WHERE [i18n:de-author] IS NOT NULL AND ISDESCENDANTNODE(n, '/cmf')" --apply-closure="\$node->getProperty('i18n:de-author')->remove();"
            bin/console doctrine:phpcr:nodes:update --query "SELECT * FROM [nt:base] AS n WHERE [i18n:en-author] IS NOT NULL AND ISDESCENDANTNODE(n, '/cmf')" --apply-closure="\$node->getProperty('i18n:en-author')->remove();" --session=live
            bin/console doctrine:phpcr:nodes:update --query "SELECT * FROM [nt:base] AS n WHERE [i18n:de-author] IS NOT NULL AND ISDESCENDANTNODE(n, '/cmf')" --apply-closure="\$node->getProperty('i18n:de-author')->remove();" --session=live
            bin/console phpcr:migrations:migrate
