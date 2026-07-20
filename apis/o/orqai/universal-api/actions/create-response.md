# Orq.ai: Create Response

Creates a response in Orq.ai.

```
POST https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "background": true,
      "id": "string",
      "input": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "model": "string",
      "object": "string",
      "output": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "status": "string",
      "store": true,
      "temperature": 1,
      "text": {
        "format": {
          "type": "string"
        },
        "verbosity": "string"
      },
      "truncation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | boolean |  |
| `id` | string |  |
| `input[].content[].text` | string |  |
| `input[].content[].type` | string |  |
| `input[].id` | string |  |
| `input[].role` | string |  |
| `input[].status` | string |  |
| `input[].type` | string |  |
| `model` | string |  |
| `object` | string |  |
| `output[].content[].text` | string |  |
| `output[].content[].type` | string |  |
| `output[].id` | string |  |
| `output[].role` | string |  |
| `output[].status` | string |  |
| `output[].type` | string |  |
| `status` | string |  |
| `store` | boolean |  |
| `temperature` | number |  |
| `text.format.type` | string |  |
| `text.verbosity` | string |  |
| `truncation` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v3/router/responses` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-response.md) for the provider-specific parameters and requirements.

