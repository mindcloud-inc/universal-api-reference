# Autotask: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/autotask/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autotask/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `isActive` | number | no |  |
| `emailAddress` | string | no | Example: `user@example.com`. |
| `phone` | string | no |  |
| `mobilePhone` | string | no |  |
| `title` | string | no |  |
| `primaryContact` | boolean | no | Making this contact primary clears the previous primary contact for the company. |
| `billingContact` | boolean | no |  |
| `receivesEmailNotifications` | boolean | no |  |
| `additionalAddressInformation` | string | no |  |
| `addressLine` | string | no |  |
| `addressLine1` | string | no |  |
| `city` | string | no |  |
| `state` | string | no |  |
| `zipCode` | string | no |  |
| `countryId` | number | no |  |
| `companyLocationId` | number | no | If address fields are blank, Autotask can populate them from this company location. |
| `alternatePhone` | string | no |  |
| `extension` | string | no |  |
| `faxNumber` | string | no |  |
| `emailAddress2` | string | no | Example: `user@example.com`. |
| `emailAddress3` | string | no | Example: `user@example.com`. |
| `externalId` | string | no |  |
| `facebookUrl` | string | no | Example: `https://example.com/profile`. |
| `linkedInUrl` | string | no | Example: `https://example.com/profile`. |
| `twitterUrl` | string | no | Example: `https://example.com/profile`. |
| `middleInitial` | string | no |  |
| `namePrefix` | number | no |  |
| `nameSuffix` | number | no |  |
| `note` | string | no | API-only note displayed in customized Contact Insight views. |
| `roomNumber` | string | no |  |
| `isOptedOutFromBulkEmail` | boolean | no |  |
| `userDefinedFields[]` | array<object> | no | Optional contact user-defined fields. |
| `userDefinedFields[].name` | string | no |  |
| `userDefinedFields[].value` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autotask API returns.

## Native endpoint

Through the native Autotask API, this operation is `PATCH /Contacts` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

