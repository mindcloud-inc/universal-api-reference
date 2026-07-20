# Klipfolio: Get Data Source Share Rights

Retrieves share rights for a Klipfolio data source.

```
GET https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-data-source-share-rights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klipfolio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-data-source-share-rights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-data-source-share-rights?${params}`, {
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
| `datasourceId` | string | no | The Klipfolio datasource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "share_rights": [
        {}
      ],
      "user_share_rights": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `share_rights` | array<object> |  |
| `user_share_rights` | array<object> |  |

## Native endpoint

Through the native Klipfolio API, this operation is `GET /datasources/:datasourceId/share-rights` (base URL `https://app.klipfolio.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-source-share-rights.md) for the provider-specific parameters and requirements.

