# AnnounceKit: List Labels

Retrieves labels for a project in AnnounceKit.

```
GET https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnnounceKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/list-labels?connectionId=$CONNECTION_ID&projectId=66505" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "66505"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/list-labels?${params}`, {
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
| `projectId` | string | yes | AnnounceKit project id used to retrieve labels. Defaults to the project id provided for this build. Default: `66505`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | AnnounceKit label id. |
| `name` | string | AnnounceKit label name. |

## Native endpoint

Through the native AnnounceKit API, this operation is `POST /gq/v2` (base URL `https://announcekit.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

