# e-Boekhouden.nl: Update Relation

Updates a relation in e-Boekhouden.nl.

```
PUT https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-relation', {
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
| `type` | string | no | Business (`B`) or Private (`P`). Defaults to `B` if empty. Error codes REL_001 Relation type is invalid (B,P). |
| `code` | string | no | The code of the relation. Auto-generated if empty. Error codes REL_049 Code already exists. REL_005 Code is invalid. REL_006 Code is too long. |
| `name` | string | yes | The (company) name of the relation. Error codes REL_002 Name is mandatory. REL_003 Name is too long. |
| `salutation` | string | no | The salutation of the relation. Error codes REL_010 Salutation is too long. |
| `contact` | string | no | The contact of the relation. Error codes REL_009 Contact is too long. |
| `gender` | string | no | Male (`m`) or female (`v`) or department (`a`) Error codes REL_004 Gender is invalid (m,v,a). |
| `address` | string | no | The primary address of the relation. Error codes REL_011 Address is too long. |
| `postalCode` | string | no | The primary postal code of the relation. Error codes REL_012 Postal code is too long. |
| `city` | string | no | The primary city of the relation. Error codes REL_013 City is too long. |
| `country` | string | no | The primary country of the relation. Error codes REL_014 Country is too long. |
| `address2` | string | no | The secondary address of the relation. Error codes REL_015 Address 2 is too long. |
| `postalCode2` | string | no | The secondary postal code of the relation. Error codes REL_016 Postal code 2 is too long. |
| `city2` | string | no | The secondary city of the relation. Error codes REL_017 City 2 is too long. |
| `country2` | string | no | The secondary country of the relation. Error codes REL_018 Country 2 is too long. |
| `phoneNumber` | string | no | The phone number of the relation. Error codes REL_019 Phone is too long. |
| `mobilePhoneNumber` | string | no | The mobile phone number of the relation. Error codes REL_020 Mobile is too long. |
| `faxNumber` | string | no | The fax number of the relation. Error codes REL_021 Fax is too long. |
| `emailAddress` | string | no | The email address of the relation. Error codes REL_022 Email is too long. REL_023 Email is invalid. |
| `emailAddressInvoice` | string | no | The invoice email address of the relation. Error codes REL_024 Email invoice is too long. REL_025 Email invoice is invalid. |
| `emailAddressReminder` | string | no | The reminder email address of the relation. Error codes REL_026 Email reminder is too long. REL_027 Email reminder is invalid. |
| `website` | string | no | The website of the relation. Error codes REL_028 Website is too long. |
| `note` | string | no | The note of the relation. |
| `vatNumber` | string | no | The VAT number of the relation. Error codes REL_035 VAT number is too long. |
| `inactive` | boolean | no | Whether the relation is inactive. |
| `termOfPayment` | number | no | The payment term of the relation. Error codes REL_030 Term of payment too low. REL_031 Term of payment too high. |
| `companyRegistrationNumber` | string | no | The company registration number of the relation. Error codes REL_008 Company registration number must be numeric. REL_050 Company registration number is too long. |
| `iban` | string | no | The IBAN number of the relation. Error codes REL_007 Iban is invalid. REL_029 Iban is too long. |
| `bic` | string | no | The BIC number of the relation. Error codes REL_032 BIC is too long. |
| `freeText1` | string | no | Free text field for the relation. Error codes REL_037 Free text 1 is too long. |
| `freeText2` | string | no | Free text field for the relation. Error codes REL_038 Free text 2 is too long. |
| `freeText3` | string | no | Free text field for the relation. Error codes REL_039 Free text 3 is too long. |
| `freeText4` | string | no | Free text field for the relation. Error codes REL_040 Free text 4 is too long. |
| `freeText5` | string | no | Free text field for the relation. Error codes REL_041 Free text 5 is too long. |
| `freeText6` | string | no | Free text field for the relation. Error codes REL_042 Free text 6 is too long. |
| `freeText7` | string | no | Free text field for the relation. Error codes REL_043 Free text 7 is too long. |
| `freeText8` | string | no | Free text field for the relation. Error codes REL_044 Free text 8 is too long. |
| `freeText9` | string | no | Free text field for the relation. Error codes REL_045 Free text 9 is too long. |
| `freeText10` | string | no | Free text field for the relation. Error codes REL_046 Free text 10 is too long. |
| `doNotReceiveNewsletters` | boolean | no | Whether the relation will receive newsletters or not. |
| `ledgerId` | number | no | The ledger ID of this relation. Error codes REL_048 Ledger not found. |
| `mandate` | boolean | no | Enable or disable mandate. |
| `mandateType` | string | no | one-time (`E`) or continuous (`D`) Error codes REL_033 Mandate type is too long. REL_051 Mandate type is invalid (E,D). |
| `mandateId` | string | no | The mandate ID of this relation. Error codes REL_034 Mandate ID is too long. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `PATCH /v1/relation/:id` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-relation.md) for the provider-specific parameters and requirements.

