# VSCO Workspace: Get Contact

Retrieves a contact from VSCO Workspace.

```
GET https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountBalance": {},
      "accountNumber": "string",
      "address": {},
      "anniversary": "2026-05-07T12:00:00.000Z",
      "anonymized": true,
      "bestDayToCall": "string",
      "bestTimeToCall": "string",
      "birthdate": "2026-05-07T12:00:00.000Z",
      "brandId": {},
      "cellPhone": {},
      "chatAccount1": {},
      "chatAccount2": {},
      "chatAccount3": {},
      "companyName": "Ava Chen",
      "contactPreference": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creditBalance": {},
      "customFields": [
        {}
      ],
      "customNumber": "string",
      "email": "ava@example.com",
      "externalMappings": [
        {}
      ],
      "facebookUsername": "Ava Chen",
      "fax": {},
      "firstName": "Ava",
      "gender": "string",
      "hidden": true,
      "homePhone": {},
      "id": "string",
      "jobTitle": "string",
      "kind": "string",
      "lastName": "Chen",
      "maidenName": "Ava Chen",
      "mailingAddress": {},
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "phone": {},
      "pinned": true,
      "previousClient": true,
      "primaryContactFirstName": "Ava",
      "primaryContactLastName": "Chen",
      "privacyOptIn": true,
      "requireStrictPrivacy": true,
      "salutation": "string",
      "schoolGradYear": 1,
      "schoolName": "Ava Chen",
      "secondaryEmail": "ava@example.com",
      "sport": "string",
      "startingCost": {},
      "startingRevenue": {},
      "teamName": "Ava Chen",
      "teamPosition": "string",
      "tollFree": {},
      "totalCost": {},
      "totalRevenue": {},
      "twitterUsername": "Ava Chen",
      "url": "https://example.com",
      "vendorRoleId": "string",
      "workPhone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountBalance` | object |  |
| `accountNumber` | string |  |
| `address` | object | Represents an address. |
| `anniversary` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `anonymized` | boolean | This person requested to be anonymized so personally identifiable information has been anonymized. |
| `bestDayToCall` | string |  |
| `bestTimeToCall` | string |  |
| `birthdate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `brandId` | object |  |
| `cellPhone` | object |  |
| `chatAccount1` | object |  |
| `chatAccount2` | object |  |
| `chatAccount3` | object |  |
| `companyName` | string |  |
| `contactPreference` | string |  |
| `created` | date | A server timestamp (always in UTC) |
| `creditBalance` | object |  |
| `customFields` | array<object> |  |
| `customNumber` | string |  |
| `email` | string |  |
| `externalMappings` | array<object> |  |
| `facebookUsername` | string |  |
| `fax` | object |  |
| `firstName` | string |  |
| `gender` | string |  |
| `hidden` | boolean | Whether or not the object is hidden. |
| `homePhone` | object |  |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `jobTitle` | string |  |
| `kind` | string |  |
| `lastName` | string |  |
| `maidenName` | string |  |
| `mailingAddress` | object | Represents an address. |
| `modified` | date | A server timestamp (always in UTC) |
| `name` | string | This is used as the combination of firstName and lastName fields. |
| `notes` | array<object> | A list of notes attached to this contact. This will only be returned in a get of a specific contact and not in the list response. |
| `phone` | object |  |
| `pinned` | boolean |  |
| `previousClient` | boolean |  |
| `primaryContactFirstName` | string |  |
| `primaryContactLastName` | string |  |
| `privacyOptIn` | boolean | Contact has Opted-In to Marketing and Processing |
| `requireStrictPrivacy` | boolean | Require Strict Privacy (e.g. subject to Europe's GDPR) |
| `salutation` | string |  |
| `schoolGradYear` | number |  |
| `schoolName` | string |  |
| `secondaryEmail` | string |  |
| `sport` | string |  |
| `startingCost` | object |  |
| `startingRevenue` | object |  |
| `teamName` | string |  |
| `teamPosition` | string |  |
| `tollFree` | object |  |
| `totalCost` | object |  |
| `totalRevenue` | object |  |
| `twitterUsername` | string |  |
| `url` | string |  |
| `vendorRoleId` | string | This is a vendor and defines the default job role does this contact have when added to a job. |
| `workPhone` | object |  |

## Native endpoint

Through the native VSCO Workspace API, this operation is `GET /address-book/:id` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

