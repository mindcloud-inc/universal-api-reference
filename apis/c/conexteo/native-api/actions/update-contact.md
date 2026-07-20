# Update Contact with Conexteo

Updates an existing contact in Conexteo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.conexteo.com`
- **Official documentation:** [Update Contact](https://developers.conexteo.com/mise-%C3%A0-jour-dun-contact-24126525e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Conexteo contact identifier. |
| `tel` | body | `string` | no | Phone number for the contact. |
| `champ_nom` | body | `string` | no | Contact last name. |
| `champ_prenom` | body | `string` | no | Contact first name. |
| `champ_mail` | body | `string` | no | Contact email address. |
| `champ_adresse` | body | `string` | no | Contact street address. |
| `champ_cp` | body | `string` | no | Contact postal code. |
| `champ_date` | body | `string` | no | Provider-formatted contact date field. |
| `champ_ville` | body | `string` | no | Contact city. |
| `champ_perso1` | body | `string` | no | Provider custom contact field 1. |
| `champ_perso2` | body | `string` | no | Provider custom contact field 2. |
| `champ_perso3` | body | `string` | no | Provider custom contact field 3. |
| `champ_perso4` | body | `string` | no | Provider custom contact field 4. |
| `champ_perso5` | body | `string` | no | Provider custom contact field 5. |
| `champ_perso6` | body | `string` | no | Provider custom contact field 6. |
| `champ_perso7` | body | `string` | no | Provider custom contact field 7. |
| `champ_perso8` | body | `string` | no | Provider custom contact field 8. |
| `champ_perso9` | body | `string` | no | Provider custom contact field 9. |
| `champ_perso10` | body | `string` | no | Provider custom contact field 10. |
