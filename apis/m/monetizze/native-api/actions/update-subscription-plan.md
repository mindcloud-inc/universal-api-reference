# Update Subscription Plan with Monetizze

Updates an existing subscription plan in Monetizze.

## Endpoint

- **Method:** `POST`
- **Path:** `/assinatura/atualizar`
- **Base URL:** `https://api.monetizze.com.br/2.1`
- **Official documentation:** [Update Subscription Plan](https://api.monetizze.com.br/2.1/apidoc/#api-Assinatura-Atualizar_Assinatura)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assinatura_id` | body | `number` | yes | Active subscription code to update. |
| `novo_plano_id` | body | `number` | yes | Target plan code for the upgrade or downgrade. |
| `politica_cobranca` | body | `string` | yes | Billing policy such as com_credito or valor_inteiro. |
| `email_consumidor` | body | `string` | yes | Subscriber email address. |
