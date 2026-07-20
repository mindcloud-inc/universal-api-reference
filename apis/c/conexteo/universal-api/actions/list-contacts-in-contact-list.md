# Conexteo: List Contacts In Contact List

Finds contacts in a Conexteo contact list.

```
GET https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-contacts-in-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-contacts-in-contact-list?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-contacts-in-contact-list?${params}`, {
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
| `id` | number | yes | Identifier of the contact list whose contacts should be listed. |

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
| `champ_adresse` | string | Street address. |
| `champ_cp` | string | Postal code. |
| `champ_date` | string | Custom date field. |
| `champ_mail` | string | Email address. |
| `champ_nom` | string | Last name. |
| `champ_perso1` | string | Custom field 1. |
| `champ_perso10` | string | Custom field 10. |
| `champ_perso2` | string | Custom field 2. |
| `champ_perso3` | string | Custom field 3. |
| `champ_perso4` | string | Custom field 4. |
| `champ_perso5` | string | Custom field 5. |
| `champ_perso6` | string | Custom field 6. |
| `champ_perso7` | string | Custom field 7. |
| `champ_perso8` | string | Custom field 8. |
| `champ_perso9` | string | Custom field 9. |
| `champ_prenom` | string | First name. |
| `champ_ville` | string | City. |
| `id` | number | Contact identifier. |
| `tel` | string | Phone number. |

## Native endpoint

Through the native Conexteo API, this operation is `GET /contactlists/:id/contacts` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts-in-contact-list.md) for the provider-specific parameters and requirements.

