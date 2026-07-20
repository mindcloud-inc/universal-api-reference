# Nyckel: Create Text Sample

Creates a text sample in Nyckel.

```
POST https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-text-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-text-sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-text-sample', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
    "data": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `functionId` | string | yes | Nyckel function identifier. |
| `data` | string | yes | Sample text content. |
| `externalId` | string | no | Optional external identifier for the sample. |
| `annotation.labelId` | string | no | Optional label ID to assign as the annotation. |
| `annotation.labelName` | string | no | Optional label name to assign as the annotation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "externalId": "string",
      "id": "string",
      "sampleSets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `sampleSets` | array<object> |  |

## Native endpoint

Through the native Nyckel API, this operation is `POST /functions/:functionId/samples` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-sample.md) for the provider-specific parameters and requirements.

