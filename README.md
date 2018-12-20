# Export CSV
Export arrays to CSV

### Install

Using composer include the repository by typing the following into a terminal

```
composer require daveismyname/exportcsv
```

### Usage

Include the composer autoloader, import the ExportCsv namespace.


```
<?php
require('vendor/autoload.php');

use Daveismyname\ExportCsv\ExportCsv;

//set filename
$filename = 'test.csv';

//set column names
$headerFields = array('First Name', 'Last Name', 'Company', 'Created');

//create array
$records = [];

//loop through data and add to array
foreach($contacts as $row) {
    $records[] = array(
        $row->firstName, 
        $row->lastName, 
        $row->companyName, 
        $row->created_at
    );
}

//OR set an array manually
$records[] = ['name', 'last name', 'comy', 'created'];

//send params to csv 
new csv($headerFields, $records, $filename);
```

Adapted from https://www.codexworld.com/export-data-to-csv-file-using-php-mysql/
