# GrowthBook: Create a single dimension

Creates a new dimension in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-dimension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-dimension" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "datasourceId": "sample_id_1",
  "identifierType": "sample",
  "query": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-dimension', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "datasourceId": "sample_id_1",
    "identifierType": "sample",
    "query": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the dimension Default: `sample`. |
| `description` | string | no | Description of the dimension |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `datasourceId` | string | yes | ID of the datasource this dimension belongs to Default: `sample_id_1`. |
| `identifierType` | string | yes | Type of identifier (user, anonymous, etc.) Default: `sample`. |
| `query` | string | yes | SQL query or equivalent for the dimension Default: `sample`. |
| `managedBy` | string | no | Where this dimension must be managed from. If not set (empty string), it can be managed from anywhere. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimension": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimension` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /dimensions` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-dimension.md) for the provider-specific parameters and requirements.

