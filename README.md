# Export CSV
Export arrays to CSV

![](https://repository-images.githubusercontent.com/162601250/24fed580-4856-11eb-8677-a058f79714c5)

### Install

Using composer include the repository by typing the following into a terminal

```
composer require dcblogdev/exportcsv
```

### Usage

Include the composer autoloader, import the ExportCsv namespace.


```php
use Dcblogdev\ExportCsv\ExportCsv;

//set filename
$filename = 'test.csv';

//set column names
$headerFields = ['First Name', 'Last Name', 'Company', 'Created'];

//create array
$records = [];

//loop through data and add to array
foreach($contacts as $row) {
    $records[] = [
        $row->firstName,
        $row->lastName,
        $row->companyName,
        $row->created_at
    ];
}

//OR set an array manually
$records[] = ['name', 'last name', 'comy', 'created'];

//send params to csv
new csv($records, $filename, $headerFields);
```

Adapted from https://www.codexworld.com/export-data-to-csv-file-using-php-mysql/
