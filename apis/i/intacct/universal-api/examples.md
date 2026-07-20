# Sage Intacct Universal API Examples

These examples use the MindCloud API key and Sage Intacct connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Custom Object



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/get-custom-object?connectionId=$CONNECTION_ID&object=CUSTOMER" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object": "CUSTOMER"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intacct/latest/actions/get-custom-object?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "ACTUALAMOUNT": {},
      "ACTUALCOMPLETIONDATE": {},
      "ACTUALQTY": "string",
      "ACTUALSTARTDATE": {},
      "APPROVEDQTY": "string",
      "BEGINDATE": {},
      "BILLABLEAPPODEFAULT": "string",
      "BILLABLEEXPDEFAULT": "string",
      "BILLINGOVERMAX": "string",
      "BILLINGPRICING": "string",
      "BILLINGRATE": {},
      "BILLINGTYPE": "string",
      "BILLTO": {
        "CONTACTNAME": {}
      },
      "BILLTOKEY": {},
      "BUDGETAMOUNT": {},
      "BUDGETEDCOST": {},
      "BUDGETID": {},
      "BUDGETKEY": {},
      "BUDGETQTY": {},
      "CLASSID": "string",
      "CLASSKEY": "string",
      "CLASSNAME": "Ava Chen",
      "CONTACTINFO": {
        "CONTACTNAME": {}
      },
      "CONTACTKEY": {},
      "CONTRACTAMOUNT": {},
      "CONTRACTID": {},
      "CONTRACTKEY": {},
      "CREATEDBY": "string",
      "CURRENCY": "string",
      "CUSTOMERID": "string",
      "CUSTOMERKEY": "string",
      "CUSTOMERNAME": "Ava Chen",
      "CUSTUSERID": {},
      "CUSTUSERKEY": {},
      "DEPARTMENTID": "string",
      "DEPARTMENTNAME": "Ava Chen",
      "DESCRIPTION": {},
      "DOCNUMBER": {},
      "ENDDATE": {},
      "ESTQTY": "string",
      "EXCLUDEEXPENSES": "string",
      "EXCLUSIONS": {},
      "EXECUTEDON": {},
      "EXPENSEPRICING": "string",
      "EXPENSERATE": "string",
      "INCLUSIONS": {},
      "INVOICECURRENCY": {},
      "INVOICEMESSAGE": {},
      "INVOICEWITHPARENT": "string",
      "LOCATIONID": "string",
      "LOCATIONNAME": "Ava Chen",
      "MANAGERCONTACTNAME": "Ava Chen",
      "MANAGERID": "string",
      "MANAGERKEY": "string",
      "MAVENLINK_ID": "https://example.com",
      "MEGAENTITYID": {},
      "MEGAENTITYKEY": {},
      "MEGAENTITYNAME": {},
      "MELOCATIONID": {},
      "MELOCATIONKEY": {},
      "MELOCATIONNAME": {},
      "MODIFIEDBY": "string",
      "NAME": "Ava Chen",
      "NOTICETOPROCEED": {},
      "OAKEY": {},
      "OBSPERCENTCOMPLETE": "string",
      "PARENTID": {},
      "PARENTKEY": {},
      "PARENTNAME": {},
      "PERCENTCOMPLETE": "string",
      "PO_NUMBER": "string",
      "POAMOUNT": {},
      "POAPPRICING": "string",
      "POAPRATE": "string",
      "PONUMBER": {},
      "POTAXSCHEDULEID": {},
      "POTAXSCHEDULEKEY": {},
      "PQNUMBER": {},
      "PREVENTAPPO": "string",
      "PREVENTEXPENSE": "string",
      "PREVENTGENINVOICE": "string",
      "PREVENTTIMESHEET": "string",
      "PRODUCT_GROUP": {},
      "PRODUCT_TYPE": {},
      "PROJECT_MANAGER_INITIALS": {},
      "PROJECTCATEGORY": "string",
      "PROJECTDEPTKEY": "string",
      "PROJECTID": "string",
      "PROJECTLOCATIONKEY": "string",
      "PROJECTSTATUS": "string",
      "PROJECTSTATUSKEY": "string",
      "PROJECTTYPE": {},
      "PROJECTTYPEKEY": {},
      "QARROWKEY": {},
      "RECORDNO": "string",
      "RED_NUCLEUS_PROJECT_ID": {},
      "REMAININGQTY": "string",
      "REPRESENTATIVE_INITIALS": {},
      "RESPONSEDUE": {},
      "REVISEDCOMPLETIONDATE": {},
      "ROLLUP_PROJ_KEY": {},
      "ROLLUPPROJECTID": {},
      "ROLLUPPROJECTNAME": {},
      "ROOTPARENTID": "string",
      "ROOTPARENTKEY": "string",
      "ROOTPARENTNAME": "Ava Chen",
      "SALESCONTACTID": {},
      "SALESCONTACTKEY": {},
      "SALESCONTACTNAME": {},
      "SCHEDULEDCOMPLETIONDATE": {},
      "SCHEDULEIMPACT": {},
      "SCHEDULESTARTDATE": {},
      "SCOPE": {},
      "SECONDARY_THERAPEUTIC_AREA": {},
      "SFDCKEY": {},
      "SHIPTO": {
        "CONTACTNAME": {}
      },
      "SHIPTOKEY": {},
      "SONUMBER": {},
      "STATUS": "string",
      "SUBSTANTIALCOMPLETIONDATE": {},
      "SUPDOCID": {},
      "SUPDOCKEY": {},
      "TAXSOLUTIONID": {},
      "TERMNAME": {},
      "TERMS": {},
      "TERMSKEY": {},
      "THERAPEUTIC_AREA": "string",
      "USERRESTRICTIONS": "string",
      "WHENCREATED": "string",
      "WHENMODIFIED": "string",
      "WIPEXCLUDE": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Custom Object action reference](actions/get-custom-object.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intacct/latest/actions/get-custom-object).

## Create Budget



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "budgetId": "2019 Annual Plan",
  "description": "string",
  "periodName": "Month Ended January 2019",
  "budgetItems[]": [
    "string"
  ],
  "budgetItems[].accountNo": "string",
  "budgetItems[].amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-budget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "budgetId": "2019 Annual Plan",
    "description": "string",
    "periodName": "Month Ended January 2019",
    "budgetItems[]": ["string"],
    "budgetItems[].accountNo": "string",
    "budgetItems[].amount": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "budgetId": "string",
      "response": {},
      "sageRecordNo": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Budget action reference](actions/create-budget.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intacct/latest/actions/create-budget).
