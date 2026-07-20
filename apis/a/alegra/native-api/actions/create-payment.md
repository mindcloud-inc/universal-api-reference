# Create Payment with Alegra

Creates a new payment in Alegra.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Create Payment](https://developer.alegra.com/reference/post_payments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date` | body | `string` | yes |
| `bankAccount.id` | body | `number` | yes |
| `paymentMethod` | body | `string` | yes |
| `observations` | body | `string` | no |
| `anotation` | body | `string` | no |
| `type` | body | `string` | no |
| `client.id` | body | `number` | no |
| `invoices[].id` | body | `number` | no |
| `invoices[].amount` | body | `number` | no |
| `invoices[].retentions[].id` | body | `number` | no |
| `invoices[].retentions[].name` | body | `string` | no |
| `invoices[].retentions[].percentage` | body | `number` | no |
| `invoices[].retentions[].amount` | body | `number` | no |
| `invoices[].retentions[].currency.code` | body | `string` | no |
| `invoices[].retentions[].currency.symbol` | body | `string` | no |
| `invoices[].retentions[].currency.exchangeRate` | body | `number` | no |
| `bills[].id` | body | `number` | no |
| `bills[].amount` | body | `number` | no |
| `bills[].retentions[].id` | body | `number` | no |
| `bills[].retentions[].name` | body | `string` | no |
| `bills[].retentions[].percentage` | body | `number` | no |
| `bills[].retentions[].amount` | body | `number` | no |
| `bills[].retentions[].currency.code` | body | `string` | no |
| `bills[].retentions[].currency.symbol` | body | `string` | no |
| `bills[].retentions[].currency.exchangeRate` | body | `number` | no |
| `categories[].id` | body | `number` | no |
| `categories[].tax.id` | body | `number` | no |
| `categories[].quantity` | body | `number` | no |
| `categories[].price` | body | `number` | no |
| `categories[].observations` | body | `string` | no |
| `retentions[].id` | body | `number` | no |
| `retentions[].amount` | body | `number` | no |
| `currency.code` | body | `string` | no |
| `currency.exchangeRate` | body | `number` | no |
| `costCenter` | body | `number` | no |
| `comments[]` | body | `array<string>` | no |
