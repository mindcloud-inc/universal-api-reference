# e-Boekhouden.nl: Update Member

Updates a member in e-Boekhouden.nl.

```
PUT https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `memberNumber` | string | no | The code of the member. Auto-generated if empty. Error codes MEM_049 Member number already exists. MEM_005 Member number is invalid. MEM_006 Member number is too long. |
| `name` | string | yes | The name of the member. Error codes MEM_002 Name is mandatory. MEM_003 Name is too long. |
| `salutation` | string | no | The salutation of the member. Error codes MEM_010 Salutation is too long. |
| `gender` | string | no | Male (`m`), female (`v`) or department ('a') Error codes MEM_004 Gender is invalid (m,v,a). |
| `address` | string | no | The primary address of the member. Error codes MEM_011 Address is too long. |
| `postalCode` | string | no | The primary postal code of the member. Error codes MEM_012 Postal code is too long. |
| `city` | string | no | The primary city of the member. Error codes MEM_013 City is too long. |
| `country` | string | no | The primary country of the member. Error codes MEM_014 Country is too long. |
| `phoneNumber` | string | no | The phone number of the member. Error codes MEM_019 Phone is too long. |
| `mobilePhoneNumber` | string | no | The mobile phone number of the member. Error codes MEM_020 Mobile is too long. |
| `faxNumber` | string | no | The fax number of the member. Error codes MEM_021 Fax is too long. |
| `emailAddress` | string | no | The email address of the member. Error codes MEM_022 Email is too long. MEM_023 Email is invalid. |
| `emailAddressInvoice` | string | no | The invoice email address of the member. Error codes MEM_024 Email invoice is too long. MEM_025 Email invoice is invalid. |
| `emailAddressReminder` | string | no | The reminder email address of the member. Error codes MEM_026 Email reminder is too long. MEM_027 Email reminder is invalid. |
| `note` | string | no | The note of the member. |
| `termOfPayment` | number | no | The payment term of the member. Error codes MEM_030 Term of payment too low. MEM_031 Term of payment too high. |
| `iban` | string | no | The IBAN number of the member. Error codes MEM_007 Iban is invalid. MEM_029 Iban is too long. |
| `bic` | string | no | The BIC number of the member. Error codes MEM_032 BIC is too long. |
| `freeText1` | string | no | Free text field for the member. Error codes MEM_037 Free text 1 is too long. |
| `freeText2` | string | no | Free text field for the member. Error codes MEM_038 Free text 2 is too long. |
| `freeText3` | string | no | Free text field for the member. Error codes MEM_039 Free text 3 is too long. |
| `freeText4` | string | no | Free text field for the member. Error codes MEM_040 Free text 4 is too long. |
| `freeText5` | string | no | Free text field for the member. Error codes MEM_041 Free text 5 is too long. |
| `freeText6` | string | no | Free text field for the member. Error codes MEM_042 Free text 6 is too long. |
| `freeText7` | string | no | Free text field for the member. Error codes MEM_043 Free text 7 is too long. |
| `freeText8` | string | no | Free text field for the member. Error codes MEM_044 Free text 8 is too long. |
| `freeText9` | string | no | Free text field for the member. Error codes MEM_045 Free text 9 is too long. |
| `freeText10` | string | no | Free text field for the member. Error codes MEM_046 Free text 10 is too long. |
| `doNotReceiveNewsletters` | boolean | no | Whether the member will receive newsletters or not. |
| `ledgerId` | number | no | The ledger ID of this member. Error codes MEM_048 Ledger not found. |
| `mandate` | boolean | no | Enable or disable mandate. |
| `mandateType` | string | no | one-time (`E`) or continuous (`D`) Error codes MEM_033 Mandate type is too long. MEM_051 Mandate type is invalid (E,D). |
| `mandateId` | string | no | The mandate ID of this member. Error codes MEM_034 Mandate ID is too long. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `PATCH /v1/member/:id` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member.md) for the provider-specific parameters and requirements.

