# Salesforge: Get Sequence Contact Sending Data

Retrieves sequence contact sending data from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-contact-sending-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-contact-sending-data?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceID=wks_989gtkhm1ir6z8hdv3gjn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-contact-sending-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceID` | string | yes | Workspace ID for the sending data query. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `sequenceIds` | list<string> | no | Only include sending data for the selected sequences. Accepts multiple values as an array. Example: `seq_q266pc1d33ozbe3et0mes`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/sending-data` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-sequence-contact-sending-data.md) for the provider-specific parameters and requirements.

