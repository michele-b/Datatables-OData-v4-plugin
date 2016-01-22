#Datatables-OData-v4-addon
Enables jQuery DataTables to read data from an OData service

## How to use

```javascript
$('table#people').dataTable({
    "oDataUrl": "/odata/People",
  	"oDataViaJsonp": false,	// set to true for cross-domain requests
    "ajax": ajaxOData,
    "serverSide": true,
    "columns": [
      { data: "Id", type: "num" },
      { data: "Name" },
      { data: "Surname" },
      { data: "BithPlace" },
      { data: "BirthDate", type: "date" }
  	],
});
```

When serverSide is set to true filtering and sorting are also performed via OData

### Notes
* Type for numeric and date columns must be set in the right way
* JQuery Globalize is a prerequisite

##Author
Michele Bersini

##Copyright and license
Copyright 2016 Michele Bersini under  [the MIT license](LICENSE).
