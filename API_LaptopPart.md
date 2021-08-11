# LaptopPart

Contains information about different laptop parts, including brand, size, weight, and associated models.

| Field | Type | Description |
| :--- | :--- | :--- |
| `id` | `int` | Unique indentifier. |
| `name` | `string` | Part name. |
| `brand` | `string` | Brand name (usually manufacturer). |
| `size` | `int` | Length of the part in inches. |
| `weight` | `int` | Weight of the part in pounds. |
| `model` | `object` | The type and model that uses the part. |

### Response Example
```
 {
      "id": 0,
      "name": "Screen",
      "brand": "Lenova",
      "size": 15,
      "weight": 5,
      "model": {
        "type": "laptop",
        "modelNo": "G500"
      }
    }
```

## Endpoints
`GET` | `https://samplesite.org/LaptopPart/{brandName}` 

Gets the Laptop part with the specific id.

[//]: # (Comment - alternatively, could list just LaptopPart/{id})

## Parameters

### Path Parameters

| Parameter | Description |
| :--- | :--- |
| {brandName} | Unique indentifier for the part object. |

### Query String Parameters

| Parameter | Type | Required/Optional | Description |
| :--- | :--- | :---: | :--- |
| size | `Integer` | Optional | If you include size, will only return parts with that size. |

## Sample Request

`curl -I -X GET "https://samplesite.org/LaptopPart/Dell?size=5"`

## Sample Response

The following is a sample response from the LaptopPart/{id} endpoint:

```
{
"LaptopPart" : [
    {
      "id": 1,
      "name": "Power Supply",
      "brand": "Dell",
      "size": 5,
      "weight": 10,
      "model": {
        "type": "desktop",
        "modelNo": "Y602"
      }
    }
  ]
}
```

### Response Definitions

This table describes each item in the response:

| Response Item | Description | Data Type |
| :--- | :--- | :--- |
| id | The id of the part. | Integer |
| name | Part name. | String |
| brand | Brand name selected based on the brand in the request. The brand name of the part (usually manufacturer). | String |
| size | Length of the part in inches. | Integer |
| weight | Weight of the part in pounds. | Integer |
| {model} | The type and model that uses the part. | Object |
| {model}/type | The type of computer. Laptop, Desktop, or AIO. | Object |
| {model}/modelNo | The model number of the computer. Assigned by manufacturer. | Object |

