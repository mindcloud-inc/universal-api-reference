# Cloze: Get Project

Retrieves a project from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-project?connectionId=$CONNECTION_ID&uniqueid=mindcloudstage3.com%3Aflat-20260318-151600" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueid": "mindcloudstage3.com:flat-20260318-151600"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-project?${params}`, {
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
| `uniqueid` | string | yes | Project unique direct identifier or custom identifier. Example: `mindcloudstage3.com:flat-20260318-151600`. |
| `team` | boolean | no | Retrieve the team relation instead of the local relation. |
| `detailed` | boolean | no | Retrieve detailed information. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "message": "string",
      "project": {
        "appLinks": [
          [
            {}
          ]
        ],
        "createdDate": "string",
        "direct": "string",
        "firstSeen": 1,
        "lastChanged": 1,
        "name": "Ava Chen",
        "segment": "string",
        "stage": "string",
        "step": "string",
        "summary": "string",
        "syncKey": "string",
        "userKey": "string",
        "views": [
          [
            "string"
          ]
        ],
        "visibility": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success. |
| `message` | string | Human-readable error description when the lookup fails. |
| `project` | object | Retrieved project. |
| `project.appLinks[]` | array<object> | External app links associated with the project. |
| `project.appLinks[].source` | string | External source domain. |
| `project.appLinks[].uniqueid` | string | External unique identifier. |
| `project.createdDate` | string | Project creation date. |
| `project.direct` | string | Direct identifier for the project. |
| `project.firstSeen` | number | UTC milliseconds when the project was first seen. |
| `project.lastChanged` | number | UTC milliseconds when the project last changed. |
| `project.name` | string | Project name. |
| `project.segment` | string | Project segment. |
| `project.stage` | string | Project stage. |
| `project.step` | string | Project next step. |
| `project.summary` | string | Project summary. |
| `project.syncKey` | string | Cloze sync key for the project. |
| `project.userKey` | string | Owning Cloze user key. |
| `project.views[]` | array<string> | Views that include the project. |
| `project.visibility` | string | Visibility of the project. |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/projects/get` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

