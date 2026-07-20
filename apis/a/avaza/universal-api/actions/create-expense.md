# Avaza: Create Expense

Creates a new expense in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileattachmentids": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileattachmentids": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expensedate` | date | no | The date of the expense entry (Required) |
| `useridfk` | number | no | UserID for a Timesheet/Expense user in Avaza. If not provided, UserEmail field must be provided |
| `useremail` | string | no | The email address of a Timesheet/Expense user in Avaza. If not provided, UserIDFK field must be provided. |
| `expensecategoryidfk` | number | no | The expense category to link the Expense to. If not provided, ExpenseCategoryName must be provided |
| `expensecategoryname` | string | no | Must match an existing expense category name otherwise a new category will be created. If left blank Expense Category ID must be provided. |
| `ischargeable` | boolean | no | aka Billable. Defaults to false if not provided. If set to true, a CustomerIDFK or CustomerName must be provided. |
| `isreimbursable` | boolean | no | Defaults to false if not provided. |
| `quantity` | number | no | Conditional - available for expenses that are assigned a unit priced based expense category. e.g Mileage |
| `customeridfk` | number | no | The Avaza Customer ID to associate the Expense with. Either this field or CustomerName can be provided. |
| `customername` | string | no | The name of an existing customer in Avaza. Must be an exact (case insensitive) match. |
| `projectidfk` | number | no | The Avaza project ID to associate the Expense with. |
| `projectname` | string | no | Can work for matching an expense to a project, but only if it's an exact match for a single project under the customer. |
| `taskidfk` | number | no | (optional) TaskID of a Task to link the new Expense to. A Customer and Project must be provided also. |
| `currencycode` | string | no | A 3-letter ISO CurrencyCode for the expense currency. (e.g. USD). If not provided, defaults to the Account base currency. |
| `exchangerate` | number | no | Optional (Only relevant if the expense currency is different to your account currency. If not provided we will look up the market exchange rate for you based on the expense date.) Exchange Rate = Expense Currency Amount / Base Currency Amount (e.g. if Expense currency is in AUD, and Base Currency is in USD, Exchange Rate = AUD $140 / USD $100 = 1.4) |
| `amount` | number | no | Expense Amount (Required). Must be &gt;= 0 |
| `taxidfk` | number | no | Avaza Tax ID the expense belongs to. If left blank then Tax Name must be provided. |
| `taxname` | string | no | Must exactly match an existing Tax Name that you have configured in Avaza Tax settings. If left blank then Tax ID must be provided. |
| `transactiontaxconfigcode` | string | no | Optional - Enter "INC" if the tax amount is included in the expense amount otherwise enter "EX" when the amount exlcudes the tax. Defaults to "Ex". The tax amount on the expense will be autocalculated. |
| `grouptripname` | string | no | Links the expense to a Grouping/Trip report. If no matching name found, creates a new Group/Trip Report name. |
| `expensepaymentmethodidfk` | number | no | (Optional) ID of Expense Payment Method. |
| `merchant` | string | no | The name of the merchant. |
| `merchanttaxnumber` | string | no | A Tax number identifier for the merchant. |
| `notes` | string | no | Expense Notes |
| `verifyandsave` | boolean | no | Pass false if creating a draft expense. True otherwise. |
| `fileattachmentids` | list<number> | yes | Array of File Attachment IDs to associate with this expense. The files need to have already been uploaded. Currently only accepts a single file. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/Expense` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

