# Update Custom Field with RD Station Marketing

## Endpoint

- **Method:** `PATCH`
- **Path:** `/platform/contacts/fields/:uuid`
- **Base URL:** `https://api.rd.services`
- **Official documentation:** [Update Custom Field](https://developers.rdstation.com/reference/patch_platform-contacts-fields-uuid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_type` | body | `list<string>` | yes | Tipo de dado do campo. Accepted values: `BOOLEAN`, `INTEGER`, `STRING`, `STRING[]`. |
| `label` | body | `object` | yes | Rótulo exibido do campo. |
| `label.pt-BR` | body | `string` | yes | Rótulo do campo em formulários no idioma pt-BR. |
| `name` | body | `object` | yes | Nome interno do campo. |
| `name.pt-BR` | body | `string` | yes | Nome interno do campo no idioma pt-BR. |
| `presentation_type` | body | `list<string>` | yes | Tipo de apresentação do campo. Accepted values: `CHECK_BOX`, `COMBO_BOX`, `EMAIL_INPUT`, `MULTIPLE_CHOICE`, `NUMBER_INPUT`, `PHONE_INPUT`, `RADIO_BUTTON`, `TEXT_AREA`, `TEXT_INPUT`, `URL_INPUT`. |
| `uuid` | path | `string` | yes | Contact field UUID in path. |
| `validation_rules` | body | `object` | no | Regras de validação do campo. |
| `validation_rules.valid_options[]` | body | `array<object>` | no | Lista de opções válidas para campos com seleção. |
| `validation_rules.valid_options[].label.pt-BR` | body | `string` | no | Rótulo da opção válida em pt-BR. |
| `validation_rules.valid_options[].value` | body | `string` | no | Valor interno da opção válida. |
