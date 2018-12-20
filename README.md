# Export CSV
Export arrays to CSV

Usage example:

```
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

//send params to csv 
csv($headerFields, $records, $filename);
```

Adapted from https://www.codexworld.com/export-data-to-csv-file-using-php-mysql/
