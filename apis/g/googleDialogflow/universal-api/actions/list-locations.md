# Google Dialogflow: List Locations

Retrieves locations from Google Dialogflow.

```
GET https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0&name=projects%2Fmy-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "name": "projects/my-project"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-locations?${params}`, {
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
| `name` | string | yes | Google Cloud project resource name, for example projects/my-project. Example: `projects/my-project`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Optional Google locations filter expression. Example: `name:us-*`. |
| `extraLocationTypes[]` | array<string> | no | Optional extra Google Cloud location types to include. Accepts multiple values as an array. Example: `GOOGLE_CLOUD_LOCATION_TYPE_REGIONAL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "locations": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `locations` | array<object> |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `GET v3/:name/locations` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

