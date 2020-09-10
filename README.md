# geocoder-french

Geocoder & reverse-geocoder for French territory. **(Fork from [geocoder-fr](https://www.npmjs.com/package/geocoder-fr))**  
>This version correct the original geocoder-fr by adding a true latitude & longitude result on geocode() method.  
>To avoid a break on the original behavior of **[geocoder-fr](https://www.npmjs.com/package/geocoder-fr)**, i decide to create this fork  
  

* No API key is required, this package use French gouv opendata API.
* Requests results are geojson formated.
* All package function are async.
* This package can be used with node or react 

## Usage

```
var geocoder = require('geocoder-french')
```

## Examples

### Get all location matching with address

```
geocoder.geocode('47 rue de l\'arquebuse 08000 charleville').then((addr)=> console.log(addr));

```

### Get all address matching with GPS lat & long (WGS84 coords)

```
geocoder.reverse(4.724433, 49.770714).then((coords)=> console.log(coords));
```

### Get most accurate location matching with address

```
geocoder.geocodeBestResult('47 rue de l\'arquebuse 08000 charleville').then((addr)=> console.log(addr));

```

### Get most accurate address matching with GPS lat & long (WGS84 coords)

```
geocoder.reverseBestResult(4.724433, 49.770714).then((coords)=> console.log(coords));
```

## Test

```
node test/test.js
```
___
>Thanks to Julien G for his great job on **[geocoder-fr](https://www.npmjs.com/package/geocoder-fr)**
