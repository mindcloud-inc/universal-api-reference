# Salesforge: Get Sequence Contacts Count

Retrieves a sequence contacts count from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-contacts-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-contacts-count?connectionId=$CONNECTION_ID&workspaceID=wks_989gtkhm1ir6z8hdv3gjn&sequenceID=seq_q266pc1d33ozbe3et0mes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "sequenceID": "seq_q266pc1d33ozbe3et0mes"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-contacts-count?${params}`, {
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
| `workspaceID` | string | yes | Workspace ID for the sequence. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `sequenceID` | string | yes | Sequence ID to count contacts for. Example: `seq_q266pc1d33ozbe3et0mes`. |
| `statuses` | list<string> | no | Only count contacts in the selected statuses. Accepts multiple values as an array. Example: `active,paused`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/count` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sequence-contacts-count.md) for the provider-specific parameters and requirements.

