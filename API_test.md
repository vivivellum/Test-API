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

## Parameters

### Path Parameters

### Query String Parameters

## Sample Request

## Sample Response


