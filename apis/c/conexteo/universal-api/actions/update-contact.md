# Conexteo: Update Contact

Updates an existing contact in Conexteo.

```
PUT https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/update-contact', {
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
| `id` | number | yes | Conexteo contact identifier. |
| `tel` | string | no | Phone number for the contact. |
| `champ_nom` | string | no | Contact last name. |
| `champ_prenom` | string | no | Contact first name. |
| `champ_mail` | string | no | Contact email address. |
| `champ_adresse` | string | no | Contact street address. |
| `champ_cp` | string | no | Contact postal code. |
| `champ_date` | string | no | Provider-formatted contact date field. |
| `champ_ville` | string | no | Contact city. |
| `champ_perso1` | string | no | Provider custom contact field 1. |
| `champ_perso2` | string | no | Provider custom contact field 2. |
| `champ_perso3` | string | no | Provider custom contact field 3. |
| `champ_perso4` | string | no | Provider custom contact field 4. |
| `champ_perso5` | string | no | Provider custom contact field 5. |
| `champ_perso6` | string | no | Provider custom contact field 6. |
| `champ_perso7` | string | no | Provider custom contact field 7. |
| `champ_perso8` | string | no | Provider custom contact field 8. |
| `champ_perso9` | string | no | Provider custom contact field 9. |
| `champ_perso10` | string | no | Provider custom contact field 10. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "champ_adresse": "string",
      "champ_cp": "string",
      "champ_date": "string",
      "champ_mail": "string",
      "champ_nom": "string",
      "champ_perso1": "string",
      "champ_perso10": "string",
      "champ_perso2": "string",
      "champ_perso3": "string",
      "champ_perso4": "string",
      "champ_perso5": "string",
      "champ_perso6": "string",
      "champ_perso7": "string",
      "champ_perso8": "string",
      "champ_perso9": "string",
      "champ_prenom": "string",
      "champ_ville": "string",
      "id": 1,
      "tel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `champ_adresse` | string | Contact street address. |
| `champ_cp` | string | Contact postal code. |
| `champ_date` | string | Provider-formatted date field. |
| `champ_mail` | string | Contact email address. |
| `champ_nom` | string | Contact last name. |
| `champ_perso1` | string | Provider custom contact field 1. |
| `champ_perso10` | string | Provider custom contact field 10. |
| `champ_perso2` | string | Provider custom contact field 2. |
| `champ_perso3` | string | Provider custom contact field 3. |
| `champ_perso4` | string | Provider custom contact field 4. |
| `champ_perso5` | string | Provider custom contact field 5. |
| `champ_perso6` | string | Provider custom contact field 6. |
| `champ_perso7` | string | Provider custom contact field 7. |
| `champ_perso8` | string | Provider custom contact field 8. |
| `champ_perso9` | string | Provider custom contact field 9. |
| `champ_prenom` | string | Contact first name. |
| `champ_ville` | string | Contact city. |
| `id` | number | Contact identifier. |
| `tel` | string | Phone number for the contact. |

## Native endpoint

Through the native Conexteo API, this operation is `PUT /contacts/:id` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

