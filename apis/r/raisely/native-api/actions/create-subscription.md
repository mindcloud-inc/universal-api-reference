# Create Subscription with Raisely

Creates a new subscription in Raisely.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Create Subscription](https://developers.raisely.com/reference/postsubscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | — |
| `anonymous` | body | `boolean` | no | True if the person's name should be hidden from donation feeds Examples: `true`, `false` |
| `card` | body | `string` | no | The gateway card ID to charge when collecting the subscription Example: `card_aabbccddeeffaabbccddeeff` |
| `count` | body | `number` | yes | The frequency of the subscription, used in conjunction with the `interval` property. For instance, a monthly subscription would have a `count` of `1` and an `interval` of `MONTH`. A fortnightly subscription would have a `count` of `2` and an `interval` of `WEEK`. Examples: `1`, `4` |
| `currency` | body | `string` | yes | ISO alpha-3 letter currency code Examples: `AUD`, `USD` |
| `customer` | body | `string` | no | The gateway customer ID (only used when importing new subscriptions) Example: `cus_xxxxxxxxxxxxxx` |
| `email` | body | `string` | yes | The user's email address. Raisely uses this as a unique identifier and will associate the subscription with an existing record if the email matches. Example: `harveymilk@example.com` |
| `firstName` | body | `string` | yes | The first name of the person Example: `Leila` |
| `fullName` | body | `string` | no | The full name of the person Example: `Leila Norma Eulalia Josefa Magistrado de Lima` |
| `interval` | body | `string` | yes | The interval of the subscriptions. See `count`. Examples: `WEEK`, `MONTH`, `YEAR` |
| `items` | body | `object<object>` | no | — |
| `amount` | body | `number` | no | `public` The amount spent on the item in the currency of the donation |
| `amountRefunded` | body | `number` | no | `public` The total amount refunded in cents for this line item, in the donation currency. |
| `attendance` | body | `string` | no | `public` Whether the donation item (ticket) has been checked in |
| `campaignAmount` | body | `number` | no | `public` The amount spent on the item in the currency of the campaign |
| `createdAt` | body | `string` | no | `public` ISO8601 created timestamp |
| `description` | body | `string` | no | `public` Description of the item |
| `includeInTotals` | body | `boolean` | no | `public` If false, the amount is not included in receipts as part of the total donation |
| `itemId` | body | `string` | no | `public` The item ID / reference |
| `originalAmount` | body | `number` | no | `public` The total amount of this line item in cents prior to any refunds, in the donation currency. Amount is tax inclusive. |
| `parentBundleItem` | body | `string` | no | `public` The item ID / reference of this ticket's parent bundle |
| `parentBundleItemDescription` | body | `string` | no | `public` The ticket's parent bundle description |
| `perkUuid` | body | `string` | no | `public` Deprecated |
| `productUuid` | body | `string` | no | `public` The uuid for the associated product or ticket. |
| `quantity` | body | `number` | no | `public` If multiple of the item, the number of items claimed |
| `status` | body | `string` | no | `public` The status of the donation item |
| `type` | body | `string` | no | `public` The item type. For most manual API calls, you should use the value `OTHER`. |
| `updatedAt` | body | `string` | no | `public` ISO8601 created timestamp |
| `uuid` | body | `string` | no | `public` Unique identifier for the item |
| `lastName` | body | `string` | yes | The last name of the person Example: `de Lima` |
| `message` | body | `string` | no | A public message left by the donor Example: `Glad to help out with the fundraising!` |
| `method` | body | `string` | yes | The payment gateway used for the subscription. Use STRIPE_INTENT for new subscriptions. Examples: `STRIPE_INTENT`, `CREDIT_CARD`, `CUSTOM`, `PAYPAL` |
| `methodType` | body | `string` | no | The type of payment method used, to distinguish between card, direct debit and digital wallet payments. Examples: `CARD`, `APPLE_PAY`, `GOOGLE_PAY`, `BROWSER_PAY`, `DD_BACS`, `DD_BECS` |
| `nextPayment` | body | `string` | no | An ISO8601 timestamp of the next payment due date. Raisely will charge the donation after this date. Example: `2020-12-03T06:52:46.330Z` |
| `preferredDay` | body | `number` | no | Stores the preferred day for the subscription to be billed on. If interval is WEEK, it's day of the week. If interval is MONTH, it's the day of the month. If interval is YEAR, it's day of the year. Example: `12345` |
| `preferredName` | body | `string` | no | The name that the person prefers to be called Example: `Norma` |
| `private` | query | `object` | no | Private values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `public` | body | `object` | no | Public values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `source` | body | `string` | no | The source of this subscription. Subscriptions created through the API should have a source of `OFFLINE`. Examples: `OFFLINE`, `ONLINE` |
| `token` | body | `string` | yes | Payment gateway token. Set to `null` when adding offline subscriptions with `card` and `customer`. Examples: `seti_xxxxxxxxxxxxxxxxxx`, `EXISTING_CARD` |
| `treatAsNewSubscription` | body | `boolean` | no | This field is only for importing new subscriptions. When false (default), the first successful charge of the card will result in a subscription.rebilled event. Set to true to change the first event to subscription.succeeded and send the Regular Donation Welcome message on the first payment after import. Examples: `true`, `false` |
