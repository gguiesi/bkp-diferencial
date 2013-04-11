bkp-diferencial
===============

## Preparação:

criar os arquivos de log e dar permissão de escrita

> sudo touch /var/log/backup_compactacao.log

> sudo chmod 777 /var/log/backup_compactacao.log

> sudo touch /var/log/backup_diferencial.log

> sudo chmod 777 /var/log/backup_diferencial.log

## Execução:

Backup geral: esse passo é necessário para fazer um bkp de tudo até agora

> ./compactar.backup

Backup diferencial: esse processo toma todos os arquivos novos das últimas 24hs e cria um tar com esse conteúdo.

> ./bkp-diff

## Inclusão do processo na cron

> 0 3 * * * sh <path do script>/bkp-diff
