# Olvy: Get Organisation

Retrieves organisation details from Olvy.

```
GET https://connect.mindcloud.co/v1/universal/olvy/latest/actions/get-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olvy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olvy/latest/actions/get-organisation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olvy/latest/actions/get-organisation?${params}`, {
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
      "data": {
        "organisation": {
          "alias": "string",
          "id": "string",
          "name": "Ava Chen",
          "website": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | GraphQL response envelope. |
| `data.organisation` | object | Organisation returned by the workspace query. |
| `data.organisation.alias` | string | Workspace alias. |
| `data.organisation.id` | string | Organisation identifier. |
| `data.organisation.name` | string | Organisation display name. |
| `data.organisation.website` | string | Organisation website URL. |

## Native endpoint

Through the native Olvy API, this operation is `POST /` (base URL `https://app.olvy.co/api/v2/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation.md) for the provider-specific parameters and requirements.

