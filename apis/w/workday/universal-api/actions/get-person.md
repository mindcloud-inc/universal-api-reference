# Workday: Get Person

Get a single person from the Workday Person API by Workday person ID.

```
GET https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-person?connectionId=$CONNECTION_ID&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-person?${params}`, {
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
| `personId` | string | yes | The Workday person ID. You can use a returned person id from Get Workers or Get People. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalNames": "Ava Chen",
      "audioNamePronunciation": "Ava Chen",
      "homeAddresses": "string",
      "homeEmails": "ava@example.com",
      "homeInstantMessengers": "string",
      "homePhones": "string",
      "homeWebAddresses": "string",
      "href": "string",
      "id": "string",
      "legalName": "Ava Chen",
      "personalInformation": "string",
      "photos": "string",
      "preferredName": "Ava Chen",
      "socialNetworks": "string",
      "universal_ID": {},
      "workAddresses": "string",
      "workEmails": "ava@example.com",
      "workInstantMessengers": "string",
      "workPhones": "string",
      "workWebAddresses": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalNames` | string | URL for the person's additional names resource. |
| `audioNamePronunciation` | string | URL for the person's audio name pronunciation resource. |
| `homeAddresses` | string | URL for the person's home addresses resource. |
| `homeEmails` | string | URL for the person's home emails resource. |
| `homeInstantMessengers` | string | URL for the person's home instant messengers resource. |
| `homePhones` | string | URL for the person's home phones resource. |
| `homeWebAddresses` | string | URL for the person's home web addresses resource. |
| `href` | string | A link to the person instance. |
| `id` | string | The id for Person. |
| `legalName` | string | URL for the person's legal name resource. |
| `personalInformation` | string | URL for the person's personal information resource. |
| `photos` | string | URL for the person's photos resource. |
| `preferredName` | string | URL for the person's preferred name resource. |
| `socialNetworks` | string | URL for the person's social networks resource. |
| `universal_ID` | object | The person's universal ID metadata when available. |
| `workAddresses` | string | URL for the person's work addresses resource. |
| `workEmails` | string | URL for the person's work emails resource. |
| `workInstantMessengers` | string | URL for the person's work instant messengers resource. |
| `workPhones` | string | URL for the person's work phones resource. |
| `workWebAddresses` | string | URL for the person's work web addresses resource. |

## Native endpoint

Through the native Workday API, this operation is `GET people/:ID` (base URL `{{credentials.restAPIBaseURL}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

