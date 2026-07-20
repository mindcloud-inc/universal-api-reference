# Sage Intacct: Get Custom Object



```
GET https://connect.mindcloud.co/v1/universal/intacct/latest/actions/get-custom-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object` | string | yes | Default: `CUSTOMER`. |
| `documentType` | string | no |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ACTUALAMOUNT` | object |  |
| `ACTUALCOMPLETIONDATE` | object |  |
| `ACTUALQTY` | string |  |
| `ACTUALSTARTDATE` | object |  |
| `APPROVEDQTY` | string |  |
| `BEGINDATE` | object |  |
| `BILLABLEAPPODEFAULT` | string |  |
| `BILLABLEEXPDEFAULT` | string |  |
| `BILLINGOVERMAX` | string |  |
| `BILLINGPRICING` | string |  |
| `BILLINGRATE` | object |  |
| `BILLINGTYPE` | string |  |
| `BILLTO.CONTACTNAME` | object |  |
| `BILLTOKEY` | object |  |
| `BUDGETAMOUNT` | object |  |
| `BUDGETEDCOST` | object |  |
| `BUDGETID` | object |  |
| `BUDGETKEY` | object |  |
| `BUDGETQTY` | object |  |
| `CLASSID` | string |  |
| `CLASSKEY` | string |  |
| `CLASSNAME` | string |  |
| `CONTACTINFO.CONTACTNAME` | object |  |
| `CONTACTKEY` | object |  |
| `CONTRACTAMOUNT` | object |  |
| `CONTRACTID` | object |  |
| `CONTRACTKEY` | object |  |
| `CREATEDBY` | string |  |
| `CURRENCY` | string |  |
| `CUSTOMERID` | string |  |
| `CUSTOMERKEY` | string |  |
| `CUSTOMERNAME` | string |  |
| `CUSTUSERID` | object |  |
| `CUSTUSERKEY` | object |  |
| `DEPARTMENTID` | string |  |
| `DEPARTMENTNAME` | string |  |
| `DESCRIPTION` | object |  |
| `DOCNUMBER` | object |  |
| `ENDDATE` | object |  |
| `ESTQTY` | string |  |
| `EXCLUDEEXPENSES` | string |  |
| `EXCLUSIONS` | object |  |
| `EXECUTEDON` | object |  |
| `EXPENSEPRICING` | string |  |
| `EXPENSERATE` | string |  |
| `INCLUSIONS` | object |  |
| `INVOICECURRENCY` | object |  |
| `INVOICEMESSAGE` | object |  |
| `INVOICEWITHPARENT` | string |  |
| `LOCATIONID` | string |  |
| `LOCATIONNAME` | string |  |
| `MANAGERCONTACTNAME` | string |  |
| `MANAGERID` | string |  |
| `MANAGERKEY` | string |  |
| `MAVENLINK_ID` | string |  |
| `MEGAENTITYID` | object |  |
| `MEGAENTITYKEY` | object |  |
| `MEGAENTITYNAME` | object |  |
| `MELOCATIONID` | object |  |
| `MELOCATIONKEY` | object |  |
| `MELOCATIONNAME` | object |  |
| `MODIFIEDBY` | string |  |
| `NAME` | string |  |
| `NOTICETOPROCEED` | object |  |
| `OAKEY` | object |  |
| `OBSPERCENTCOMPLETE` | string |  |
| `PARENTID` | object |  |
| `PARENTKEY` | object |  |
| `PARENTNAME` | object |  |
| `PERCENTCOMPLETE` | string |  |
| `PO_NUMBER` | string |  |
| `POAMOUNT` | object |  |
| `POAPPRICING` | string |  |
| `POAPRATE` | string |  |
| `PONUMBER` | object |  |
| `POTAXSCHEDULEID` | object |  |
| `POTAXSCHEDULEKEY` | object |  |
| `PQNUMBER` | object |  |
| `PREVENTAPPO` | string |  |
| `PREVENTEXPENSE` | string |  |
| `PREVENTGENINVOICE` | string |  |
| `PREVENTTIMESHEET` | string |  |
| `PRODUCT_GROUP` | object |  |
| `PRODUCT_TYPE` | object |  |
| `PROJECT_MANAGER_INITIALS` | object |  |
| `PROJECTCATEGORY` | string |  |
| `PROJECTDEPTKEY` | string |  |
| `PROJECTID` | string |  |
| `PROJECTLOCATIONKEY` | string |  |
| `PROJECTSTATUS` | string |  |
| `PROJECTSTATUSKEY` | string |  |
| `PROJECTTYPE` | object |  |
| `PROJECTTYPEKEY` | object |  |
| `QARROWKEY` | object |  |
| `RECORDNO` | string |  |
| `RED_NUCLEUS_PROJECT_ID` | object |  |
| `REMAININGQTY` | string |  |
| `REPRESENTATIVE_INITIALS` | object |  |
| `RESPONSEDUE` | object |  |
| `REVISEDCOMPLETIONDATE` | object |  |
| `ROLLUP_PROJ_KEY` | object |  |
| `ROLLUPPROJECTID` | object |  |
| `ROLLUPPROJECTNAME` | object |  |
| `ROOTPARENTID` | string |  |
| `ROOTPARENTKEY` | string |  |
| `ROOTPARENTNAME` | string |  |
| `SALESCONTACTID` | object |  |
| `SALESCONTACTKEY` | object |  |
| `SALESCONTACTNAME` | object |  |
| `SCHEDULEDCOMPLETIONDATE` | object |  |
| `SCHEDULEIMPACT` | object |  |
| `SCHEDULESTARTDATE` | object |  |
| `SCOPE` | object |  |
| `SECONDARY_THERAPEUTIC_AREA` | object |  |
| `SFDCKEY` | object |  |
| `SHIPTO.CONTACTNAME` | object |  |
| `SHIPTOKEY` | object |  |
| `SONUMBER` | object |  |
| `STATUS` | string |  |
| `SUBSTANTIALCOMPLETIONDATE` | object |  |
| `SUPDOCID` | object |  |
| `SUPDOCKEY` | object |  |
| `TAXSOLUTIONID` | object |  |
| `TERMNAME` | object |  |
| `TERMS` | object |  |
| `TERMSKEY` | object |  |
| `THERAPEUTIC_AREA` | string |  |
| `USERRESTRICTIONS` | string |  |
| `WHENCREATED` | string |  |
| `WHENMODIFIED` | string |  |
| `WIPEXCLUDE` | string |  |

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-object.md) for the provider-specific parameters and requirements.

