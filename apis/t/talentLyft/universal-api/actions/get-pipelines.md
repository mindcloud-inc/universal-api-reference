# TalentLyft: Get Pipelines

Retrieves all pipelines from TalentLyft.

```
GET https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLyft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-pipelines?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TalentLyft API returns.

## Native endpoint

Through the native TalentLyft API, this operation is `GET /v2/pipelines` (base URL `https://api.talentlyft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipelines.md) for the provider-specific parameters and requirements.

