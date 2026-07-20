# Process Plan: Convert Results IDs to Objects



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-results-i-ds-to-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-results-i-ds-to-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-results-i-ds-to-objects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "text_value_list": [
        {
          "text": "string",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text_value_list[].text` | string |  |
| `text_value_list[].value` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `POST /id_list/to_object/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-results-i-ds-to-objects.md) for the provider-specific parameters and requirements.

