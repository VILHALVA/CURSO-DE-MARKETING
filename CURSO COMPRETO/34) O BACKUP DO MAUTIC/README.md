# O BACKUP DO MAUTIC
Fazer backups regulares do Mautic é uma prática importante para garantir a segurança dos seus dados e a capacidade de recuperar informações em caso de falhas no sistema. Aqui estão os passos para fazer o backup do Mautic e restaurar o banco de dados:

**Fazendo o Backup do Mautic via SSH:**

1. Conecte-se ao servidor onde o Mautic está hospedado via SSH usando um cliente SSH, como o PuTTY, se você estiver em um ambiente Linux ou macOS, ou o PuTTY se estiver em um ambiente Windows.

2. Acesse a pasta do Mautic no servidor usando o comando `cd` para navegar até o diretório do Mautic.

3. Use o utilitário `mysqldump` para criar um backup do banco de dados do Mautic. O comando geralmente terá a seguinte estrutura:

   ```bash
   mysqldump -u [seu_usuario] -p[sua_senha] [nome_do_banco] > backup_mautic.sql
   ```

   - `[seu_usuario]` é o nome de usuário do banco de dados do Mautic.
   - `[sua_senha]` é a senha do usuário do banco de dados.
   - `[nome_do_banco]` é o nome do banco de dados do Mautic.
   - `backup_mautic.sql` é o nome do arquivo de backup que você deseja criar.

4. O comando irá criar um arquivo SQL contendo o backup do banco de dados do Mautic no diretório atual.

**Restaurando o Banco de Dados do Mautic:**

1. Para restaurar o banco de dados, você precisará acessar o servidor e navegar até a pasta onde o arquivo de backup SQL está localizado.

2. Use o comando `mysql` para importar o arquivo de backup para o banco de dados. O comando geralmente terá a seguinte estrutura:

   ```bash
   mysql -u [seu_usuario] -p[sua_senha] [nome_do_banco] < backup_mautic.sql
   ```

   Certifique-se de substituir `[seu_usuario]`, `[sua_senha]`, `[nome_do_banco]` e `backup_mautic.sql` pelos valores apropriados.

3. O banco de dados será restaurado a partir do arquivo de backup.

Lembre-se de que fazer backups regulares é essencial para a segurança e a integridade dos seus dados. Certifique-se de armazenar os backups em locais seguros e, se possível, automatizar o processo de backup para garantir que você sempre tenha cópias atualizadas dos seus dados do Mautic disponíveis em caso de problemas.