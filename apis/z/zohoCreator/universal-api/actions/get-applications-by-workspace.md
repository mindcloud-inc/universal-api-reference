# Zoho Creator: Get Applications by Workspace

Retrieves workspace applications from Zoho Creator.

```
GET https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications-by-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications-by-workspace?connectionId=$CONNECTION_ID&accountOwnerName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountOwnerName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications-by-workspace?${params}`, {
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
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applications": [
        {}
      ],
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applications` | array<object> | Applications visible inside the selected Zoho Creator workspace. |
| `code` | number | Zoho Creator response code. |

## Native endpoint

Through the native Zoho Creator API, this operation is `GET /meta/:account_owner_name/applications` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applications-by-workspace.md) for the provider-specific parameters and requirements.

