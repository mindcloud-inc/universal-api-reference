# Filestage: List File Reviews by Parameters

Finds Filestage file reviews by parameter.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-file-reviews-by-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-file-reviews-by-parameters?connectionId=$CONNECTION_ID&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-file-reviews-by-parameters?${params}`, {
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
| `externalId` | string | yes | `externalId` of the file |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stepId` | string | no | Step Id to filter results by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "decisions": [
        {}
      ],
      "dueDate": "2026-05-07T12:00:00.000Z",
      "fileId": "string",
      "id": "string",
      "status": {
        "state": "string"
      },
      "stepId": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `decisions` | array<object> |  |
| `dueDate` | date |  |
| `fileId` | string |  |
| `id` | string |  |
| `status` | object |  |
| `status.state` | string |  |
| `stepId` | string |  |
| `versionId` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `GET /files/reviews` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-reviews-by-parameters.md) for the provider-specific parameters and requirements.

