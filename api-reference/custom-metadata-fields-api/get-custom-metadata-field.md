# Get custom metadata field

{% swagger baseUrl="https://api.imagekit.io" path="/v1/customMetadataFields" method="get" summary="Get existing custom metadata fields" %}
{% swagger-description %}
Get a list of all the custom metadata fields.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
base64 encoding of `your_private_api_key:`

**Note the colon in the end.**
{% endswagger-parameter %}

{% swagger-parameter in="query" name="includeDeleted" %}
Set it to `true` if you want to receive deleted fields as well in the API response.
{% endswagger-parameter %}

{% swagger-response status="200" description="In the response, you will get an array of all the custom metadata fields with each object having field id, name, label and schema." %}
```javascript
[
    {
        "id": "598821f949c0a938d57563dd",
        "name": "brand",
        "label": "brand",
        "schema": {
            "type": "Text",
            "defaultValue": "Nike"
        }
    },
    {
        "id": "865421f949c0a835d57563dd"
        "name": "price",
        "label": "price",
        "schema": {
            "type": "Number",
            "minValue": 1000,
            "maxValue": 3000
        }
    }
]
```
{% endswagger-response %}
{% endswagger %}



## Examples

{% tabs %}
{% tab title="cURL" %}
```basic
curl -X GET "https://api.imagekit.io/v1/customMetadataFields" \
-H 'Content-Type: application/json' \
-u your_private_key:
```
{% endtab %}
{% endtabs %}