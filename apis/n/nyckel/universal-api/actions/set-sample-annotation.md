# Nyckel: Set Sample Annotation

Updates a sample annotation in Nyckel.

```
PUT https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/set-sample-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/set-sample-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "sampleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/set-sample-annotation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
    "sampleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `functionId` | string | yes | Nyckel function identifier. |
| `sampleId` | string | yes | Nyckel sample identifier. |
| `labelId` | string | no | Label ID to set as the sample annotation. |
| `labelName` | string | no | Label name to set as the sample annotation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "labelId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `labelId` | string |  |

## Native endpoint

Through the native Nyckel API, this operation is `PUT /functions/:functionId/samples/:sampleId/annotation` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-sample-annotation.md) for the provider-specific parameters and requirements.

