# WORKSHOP_PHP

1. WampServer
    - URL to Download : https://sourceforge.net/projects/wampserver/files/WampServer%203/WampServer%203.0.0/wampserver3.1.7_x64.exe/download
    - Start services 
    - Go to http://localhost
    - Create new directory "Workshop_PHP" in directory (C:\wamp\www)
    - Create a new file "workshop.php" in the directory
    
2. PhpMyAdmin
    - Log with User = "root" and without password
    - Create a new Database ("workshop")
    - Create a new Table in workshop database ("user") with 5 colomns : 
        - id        - int(11)       - AUTO_INCREMENT(A.I)
        - firstname - varchar(255)
        - lastname  - varchar(255)
        - mail      - varchar(255)
        - phone     - varchar(255)

3. Script PHP
    - Connect to your Database 
    ```php
    $bdd = new PDO('mysql:host=localhost;dbname=workshop;charset=utf8', 'root', '');
    ```
    - Write data
    ```php
    $bdd->exec("INSERT INTO ...");
    ```
    - Read data
    ```php
    $reponse = $bdd->query('SELECT * FROM user');
    ```
