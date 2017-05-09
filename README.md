## Bina direktori (*)

- <your_app_foler>

-- config

-- controllers

-- db (*)

--- oci (*)

Letak fail ESchemaOci.php dalam folder "oci"


Kemaskini fail config/db.php anda kepada seperti dibawah : 

return [
    'class' => 'yii\db\Connection',
    'dsn' => 'oci:dbname=(DESCRIPTION=(ADDRESS_LIST=(ADDRESS=(PROTOCOL=TCP)(HOST=192.168.1.1)(PORT=1521)))(CONNECT_DATA=(SERVICE_NAME=TNSNAME)));charset=UTF8;',
    'username' => 'USERNAME',
    'password' => 'PASSWORD',
    'attributes' => [PDO::ATTR_CASE => PDO::CASE_LOWER],
    'schemaMap'=>['oci'=>'app\db\oci\ESchemaOci',],
];
