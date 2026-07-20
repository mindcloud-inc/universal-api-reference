# Nutshell: Get Contact

Retrieves a contact from Nutshell.

```
GET https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutshell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The Nutshell contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "isPrimary": true,
          "name": "Ava Chen",
          "value": {
            "address1": "string",
            "address2": {},
            "address3": {},
            "city": "string",
            "country": "string",
            "location": {
              "latitude": 1,
              "longitude": 1
            },
            "locationAccuracy": "string",
            "postalCode": "string",
            "state": "string",
            "timezone": {}
          }
        }
      ],
      "avatarUrl": "https://example.com",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "deletedTime": {},
      "description": "string",
      "emails": [
        {
          "isPrimary": true,
          "name": "ava@example.com",
          "value": "ava@example.com"
        }
      ],
      "firstName": "Ava",
      "href": "string",
      "htmlUrl": "https://example.com",
      "htmlUrlPath": "https://example.com",
      "id": "string",
      "initials": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "links": {
        "accounts": [
          "https://example.com"
        ],
        "creator": {},
        "followup": {},
        "mergedWith": {},
        "origin": "https://example.com",
        "owner": {},
        "recurringTask": {},
        "territory": {}
      },
      "mcfxContactId": {},
      "name": "Ava Chen",
      "type": "string",
      "urls": [
        {
          "isPrimary": true,
          "name": "https://example.com",
          "value": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].isPrimary` | boolean |  |
| `addresses[].name` | string |  |
| `addresses[].value.address1` | string |  |
| `addresses[].value.address2` | object |  |
| `addresses[].value.address3` | object |  |
| `addresses[].value.city` | string |  |
| `addresses[].value.country` | string |  |
| `addresses[].value.location.latitude` | number |  |
| `addresses[].value.location.longitude` | number |  |
| `addresses[].value.locationAccuracy` | string |  |
| `addresses[].value.postalCode` | string |  |
| `addresses[].value.state` | string |  |
| `addresses[].value.timezone` | object |  |
| `avatarUrl` | string |  |
| `createdTime` | date |  |
| `deletedTime` | object |  |
| `description` | string |  |
| `emails[].isPrimary` | boolean |  |
| `emails[].name` | string |  |
| `emails[].value` | string |  |
| `firstName` | string |  |
| `href` | string |  |
| `htmlUrl` | string |  |
| `htmlUrlPath` | string |  |
| `id` | string |  |
| `initials` | string |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `links.accounts[]` | string |  |
| `links.creator` | object |  |
| `links.followup` | object |  |
| `links.mergedWith` | object |  |
| `links.origin` | string |  |
| `links.owner` | object |  |
| `links.recurringTask` | object |  |
| `links.territory` | object |  |
| `mcfxContactId` | object |  |
| `name` | string |  |
| `type` | string |  |
| `urls[].isPrimary` | boolean |  |
| `urls[].name` | string |  |
| `urls[].value` | string |  |

## Native endpoint

Through the native Nutshell API, this operation is `GET /contacts/:id` (base URL `https://app.nutshell.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

