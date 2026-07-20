# Astra: List Databases

Retrieves database records from Astra.

```
GET https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-databases?${params}`, {
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
      "creationTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "info": {},
      "metrics": {},
      "observedStatus": "string",
      "orgId": "string",
      "ownerId": "string",
      "status": "string",
      "terminationTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationTime` | date | When the database was created. |
| `id` | string | The Astra database ID. |
| `info` | object | Database metadata including name, region, tier, and datacenter details. |
| `metrics` | object | Usage and error counters for the database. |
| `observedStatus` | string | The observed database lifecycle status. |
| `orgId` | string | The owning organization ID. |
| `ownerId` | string | The owning principal ID. |
| `status` | string | The database lifecycle status. |
| `terminationTime` | date | When the database is scheduled for termination. |

## Native endpoint

Through the native Astra API, this operation is `GET /v2/databases` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-databases.md) for the provider-specific parameters and requirements.

