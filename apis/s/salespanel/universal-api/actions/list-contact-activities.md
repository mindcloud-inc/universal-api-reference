# Salespanel: List Contact Activities

Retrieves activities for a contact in Salespanel by ID or email.

```
GET https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-contact-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salespanel `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-contact-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-contact-activities?${params}`, {
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
| `contactId` | string | yes | The unique ID of the contact whose activities you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityIdentifier": "string",
      "activityType": "string",
      "category": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "form": true,
      "label": "string",
      "link": "https://example.com",
      "metadata": {
        "loggedIn": true,
        "pageUrl": "https://example.com",
        "videoId": "string"
      },
      "pageDuration": 1,
      "pageTitle": "string",
      "referrerLink": "https://example.com",
      "subject": "string",
      "utmParams": {
        "utmSource": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityIdentifier` | string |  |
| `activityType` | string |  |
| `category` | string |  |
| `createdOn` | date |  |
| `form` | boolean |  |
| `label` | string |  |
| `link` | string |  |
| `metadata.loggedIn` | boolean |  |
| `metadata.pageUrl` | string |  |
| `metadata.videoId` | string |  |
| `pageDuration` | number |  |
| `pageTitle` | string |  |
| `referrerLink` | string |  |
| `subject` | string |  |
| `utmParams.utmSource` | string |  |

## Native endpoint

Through the native Salespanel API, this operation is `GET /contacts/:contact_id/activities/` (base URL `https://salespanel.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-activities.md) for the provider-specific parameters and requirements.

