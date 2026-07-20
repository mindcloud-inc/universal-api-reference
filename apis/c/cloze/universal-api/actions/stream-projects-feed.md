# Cloze: Stream Projects Feed

Retrieves the projects feed from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/stream-projects-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/stream-projects-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/stream-projects-feed?${params}`, {
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
| `cursor` | string | no | Cursor to the next batch of results from the previous feed response. |
| `freeformquery` | string | no | Natural language query expression. |
| `modifiedafter` | string | no | Starting point in UTC milliseconds for change polling. |
| `scope` | string | no | Project scope selector. |
| `segment` | string | no | Project segment selector. |
| `stage` | string | no | Project stage selector. |
| `keysonly` | boolean | no | Return just the syncKey field. |
| `includeauditedchanges` | boolean | no | Include audited changes in feed results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availablecount": 1,
      "cursor": "string",
      "errorcode": 1,
      "projects": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availablecount` | number | Number of projects returned in this batch. |
| `cursor` | string | Cursor to use for the next feed request. |
| `errorcode` | number | Error code. 0 means success. |
| `projects[]` | array<object> | Projects delivered in this batch. |
| `projects[].appLinks[]` | array<object> | External app links associated with the project. |
| `projects[].appLinks[].source` | string | External source domain. |
| `projects[].appLinks[].uniqueid` | string | External unique identifier. |
| `projects[].createdDate` | string | Project creation date. |
| `projects[].direct` | string | Direct identifier for the project. |
| `projects[].firstSeen` | number | UTC milliseconds when the project was first seen. |
| `projects[].lastChanged` | number | UTC milliseconds when the project last changed. |
| `projects[].name` | string | Project name. |
| `projects[].segment` | string | Project segment. |
| `projects[].stage` | string | Project stage. |
| `projects[].step` | string | Project next step. |
| `projects[].summary` | string | Project summary. |
| `projects[].syncKey` | string | Cloze sync key for the project. |
| `projects[].userKey` | string | Owning Cloze user key. |
| `projects[].views[]` | array<string> | Views that include the project. |
| `projects[].visibility` | string | Visibility of the project. |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/projects/feed` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-projects-feed.md) for the provider-specific parameters and requirements.

