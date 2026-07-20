# Update Contact with eTermin

Updates an existing contact in eTermin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/contact`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Update Contact](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Contact/put_api_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salutation` | query | `string` | no | Salutation of the person. |
| `title` | query | `string` | no | Title of the person. |
| `lastname` | query | `string` | no | Lastname of the person. |
| `birthday` | query | `string` | no | Birthday of the person. |
| `email` | query | `string` | no | E-Mail of the person. |
| `phone` | query | `string` | no | Phone of the person. |
| `company` | query | `string` | no | Company of the person (make sure this field exists in your account) |
| `street` | query | `string` | no | Street of the person. |
| `zip` | query | `string` | no | Zip of the person. |
| `city` | query | `string` | no | City of the person. |
| `state` | query | `string` | no | State of the person. |
| `country` | query | `string` | no | Country of the person. |
| `customernumber` | query | `string` | no | ID of the person. |
| `loginid` | query | `string` | no | Sets the loginID for the contact (if Login is used on Bookingpage). |
| `password` | query | `string` | no | Sets the initial password for the contact. |
| `newsletter` | query | `boolean` | no | Opts the contact into the newsletter. |
| `additional1` | query | `string` | no | Additional appointment field 1. |
| `additional2` | query | `string` | no | Additional appointment field 2. |
| `additional3` | query | `string` | no | Additional appointment field 3. |
| `additional4` | query | `string` | no | Additional appointment field 4. |
| `additional5` | query | `string` | no | Additional appointment field 5. |
| `additional6` | query | `string` | no | Additional appointment field 6. |
| `additional7` | query | `string` | no | Additional appointment field 7. |
| `additional8` | query | `string` | no | Additional appointment field 8. |
| `additional9` | query | `string` | no | Additional appointment field 9. |
| `additional10` | query | `string` | no | Additional appointment field 10. |
| `additional11` | query | `string` | no | Additional appointment field 11. |
| `additional12` | query | `string` | no | Additional appointment field 12. |
| `additional13` | query | `string` | no | Additional appointment field 13. |
| `additional14` | query | `string` | no | Additional appointment field 14. |
| `additional15` | query | `string` | no | Additional appointment field 15. |
| `additional16` | query | `string` | no | Additional appointment field 16. |
| `additional17` | query | `string` | no | Additional appointment field 17. |
| `additional18` | query | `string` | no | Additional appointment field 18. |
| `additional19` | query | `string` | no | Additional appointment field 19. |
| `additional20` | query | `string` | no | Additional appointment field 20. |
| `tags` | query | `string` | no | Tags of the person. To add multiple tags use a comma (,) |
