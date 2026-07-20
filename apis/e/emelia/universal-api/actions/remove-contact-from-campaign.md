# Emelia: Remove Contact From Campaign

Deletes a contact from an Emelia campaign by email.

```
DELETE https://connect.mindcloud.co/v1/universal/emelia/latest/actions/remove-contact-from-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/remove-contact-from-campaign?connectionId=$CONNECTION_ID&email=ava%40example.com&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/remove-contact-from-campaign?${params}`, {
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
| `email` | string | yes | Contact email address |
| `id` | string | yes | Campaign identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "removeOneContactFromCampaign": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.removeOneContactFromCampaign` | boolean |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-from-campaign.md) for the provider-specific parameters and requirements.

