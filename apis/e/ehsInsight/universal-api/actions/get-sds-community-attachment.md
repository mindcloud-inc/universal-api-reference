# EHS Insight: Get SDS Community Attachment



```
GET https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-sds-community-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-sds-community-attachment?connectionId=$CONNECTION_ID&rowUid=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowUid": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-sds-community-attachment?${params}`, {
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
| `rowUid` | string | yes | Identifier of the SDS Community attachment to download. SDS means safety data sheet. Example: `550e8400-e29b-41d4-a716-446655440000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EHS Insight API returns.

## Native endpoint

Through the native EHS Insight API, this operation is `GET /v6/sdscommunity/attachment/fetch/:rowUid` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sds-community-attachment.md) for the provider-specific parameters and requirements.

