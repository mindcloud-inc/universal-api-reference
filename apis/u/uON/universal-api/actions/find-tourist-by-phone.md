# U-ON: Find Tourist by Phone

Finds a tourist in U-ON by phone number.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/find-tourist-by-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/find-tourist-by-phone?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/find-tourist-by-phone?${params}`, {
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
| `phone` | string | yes | phone path parameter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "address": "string",
      "address_juridical": "string",
      "bcard_id": "string",
      "bcard_number": "string",
      "bcard_value": "string",
      "cabinet_created": 1,
      "cabinet_created_date": "string",
      "deleted": 1,
      "delivery_subscription": 1,
      "extended_fields": [
        "string"
      ],
      "files": [
        "string"
      ],
      "global_u_id": 1,
      "ip_internal_number": "string",
      "labels": "string",
      "manager_id": 1,
      "nationality": "string",
      "nationality_id": "string",
      "notifications": 1,
      "office_id": "string",
      "role_id": 1,
      "source_id": 1,
      "timezone": "string",
      "tourist_kind": "string",
      "u_birthday": "string",
      "u_birthday_certificate": "string",
      "u_birthday_certificate_given": "string",
      "u_birthday_certificate_organization": "string",
      "u_birthday_place": "string",
      "u_company": "string",
      "u_date_update": "string",
      "u_discount": "string",
      "u_email": "ava@example.com",
      "u_fax": "string",
      "u_finance_bank": "string",
      "u_finance_bik": "string",
      "u_finance_ks": "string",
      "u_finance_okpo": "string",
      "u_finance_rs": "string",
      "u_id": 1,
      "u_image": "string",
      "u_inn": "string",
      "u_instagram": "string",
      "u_kpp": "string",
      "u_manager_status": 1,
      "u_max": "string",
      "u_name": "Ava Chen",
      "u_name_en": "Ava Chen",
      "u_note": "string",
      "u_ogrn": "string",
      "u_okved": "string",
      "u_passport_code": "string",
      "u_passport_date": "string",
      "u_passport_number": "string",
      "u_passport_taken": "string",
      "u_phone": "string",
      "u_phone_home": "string",
      "u_phone_mobile": "string",
      "u_position": "string",
      "u_sex": 1,
      "u_sname": "Ava Chen",
      "u_social_fb": "string",
      "u_social_ok": "string",
      "u_social_vk": "string",
      "u_surname": "Ava Chen",
      "u_surname_en": "Ava Chen",
      "u_telegram": "string",
      "u_type": 1,
      "u_viber": "string",
      "u_whatsapp": "string",
      "u_zagran_expire": "string",
      "u_zagran_given": "string",
      "u_zagran_number": "string",
      "u_zagran_organization": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | U-ON tourist runtime field: active |
| `address` | string | U-ON tourist runtime field: address |
| `address_juridical` | string | U-ON tourist runtime field: address_juridical |
| `bcard_id` | string | U-ON tourist runtime field: bcard_id |
| `bcard_number` | string | U-ON tourist runtime field: bcard_number |
| `bcard_value` | string | U-ON tourist runtime field: bcard_value |
| `cabinet_created` | number | U-ON tourist runtime field: cabinet_created |
| `cabinet_created_date` | string | U-ON tourist runtime field: cabinet_created_date |
| `deleted` | number | U-ON tourist runtime field: deleted |
| `delivery_subscription` | number | U-ON tourist runtime field: delivery_subscription |
| `extended_fields` | array | U-ON tourist runtime field: extended_fields |
| `files` | array | U-ON tourist runtime field: files |
| `global_u_id` | number | U-ON tourist runtime field: global_u_id |
| `ip_internal_number` | string | U-ON tourist runtime field: ip_internal_number |
| `labels` | string | U-ON tourist runtime field: labels |
| `manager_id` | number | U-ON tourist runtime field: manager_id |
| `nationality` | string | U-ON tourist runtime field: nationality |
| `nationality_id` | string | U-ON tourist runtime field: nationality_id |
| `notifications` | number | U-ON tourist runtime field: notifications |
| `office_id` | string | U-ON tourist runtime field: office_id |
| `role_id` | number | U-ON tourist runtime field: role_id |
| `source_id` | number | U-ON tourist runtime field: source_id |
| `timezone` | string | U-ON tourist runtime field: timezone |
| `tourist_kind` | string | U-ON tourist runtime field: tourist_kind |
| `u_birthday` | string | U-ON tourist runtime field: u_birthday |
| `u_birthday_certificate` | string | U-ON tourist runtime field: u_birthday_certificate |
| `u_birthday_certificate_given` | string | U-ON tourist runtime field: u_birthday_certificate_given |
| `u_birthday_certificate_organization` | string | U-ON tourist runtime field: u_birthday_certificate_organization |
| `u_birthday_place` | string | U-ON tourist runtime field: u_birthday_place |
| `u_company` | string | U-ON tourist runtime field: u_company |
| `u_date_update` | string | U-ON tourist runtime field: u_date_update |
| `u_discount` | string | U-ON tourist runtime field: u_discount |
| `u_email` | string | U-ON tourist runtime field: u_email |
| `u_fax` | string | U-ON tourist runtime field: u_fax |
| `u_finance_bank` | string | U-ON tourist runtime field: u_finance_bank |
| `u_finance_bik` | string | U-ON tourist runtime field: u_finance_bik |
| `u_finance_ks` | string | U-ON tourist runtime field: u_finance_ks |
| `u_finance_okpo` | string | U-ON tourist runtime field: u_finance_okpo |
| `u_finance_rs` | string | U-ON tourist runtime field: u_finance_rs |
| `u_id` | number | U-ON tourist runtime field: u_id |
| `u_image` | string | U-ON tourist runtime field: u_image |
| `u_inn` | string | U-ON tourist runtime field: u_inn |
| `u_instagram` | string | U-ON tourist runtime field: u_instagram |
| `u_kpp` | string | U-ON tourist runtime field: u_kpp |
| `u_manager_status` | number | U-ON tourist runtime field: u_manager_status |
| `u_max` | string | U-ON tourist runtime field: u_max |
| `u_name` | string | U-ON tourist runtime field: u_name |
| `u_name_en` | string | U-ON tourist runtime field: u_name_en |
| `u_note` | string | U-ON tourist runtime field: u_note |
| `u_ogrn` | string | U-ON tourist runtime field: u_ogrn |
| `u_okved` | string | U-ON tourist runtime field: u_okved |
| `u_passport_code` | string | U-ON tourist runtime field: u_passport_code |
| `u_passport_date` | string | U-ON tourist runtime field: u_passport_date |
| `u_passport_number` | string | U-ON tourist runtime field: u_passport_number |
| `u_passport_taken` | string | U-ON tourist runtime field: u_passport_taken |
| `u_phone` | string | U-ON tourist runtime field: u_phone |
| `u_phone_home` | string | U-ON tourist runtime field: u_phone_home |
| `u_phone_mobile` | string | U-ON tourist runtime field: u_phone_mobile |
| `u_position` | string | U-ON tourist runtime field: u_position |
| `u_sex` | number | U-ON tourist runtime field: u_sex |
| `u_sname` | string | U-ON tourist runtime field: u_sname |
| `u_social_fb` | string | U-ON tourist runtime field: u_social_fb |
| `u_social_ok` | string | U-ON tourist runtime field: u_social_ok |
| `u_social_vk` | string | U-ON tourist runtime field: u_social_vk |
| `u_surname` | string | U-ON tourist runtime field: u_surname |
| `u_surname_en` | string | U-ON tourist runtime field: u_surname_en |
| `u_telegram` | string | U-ON tourist runtime field: u_telegram |
| `u_type` | number | U-ON tourist runtime field: u_type |
| `u_viber` | string | U-ON tourist runtime field: u_viber |
| `u_whatsapp` | string | U-ON tourist runtime field: u_whatsapp |
| `u_zagran_expire` | string | U-ON tourist runtime field: u_zagran_expire |
| `u_zagran_given` | string | U-ON tourist runtime field: u_zagran_given |
| `u_zagran_number` | string | U-ON tourist runtime field: u_zagran_number |
| `u_zagran_organization` | string | U-ON tourist runtime field: u_zagran_organization |

## Native endpoint

Through the native U-ON API, this operation is `GET /user/phone/{phone}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-tourist-by-phone.md) for the provider-specific parameters and requirements.

