# PAYable – Manual Fetch of Merchant Notification Details

---

## Required details

You can grab the following from the merchant portal:

| Parameter | Required |
|-----------|----------|
| **orderId** | Yes |

---

## Refund Status API

**Endpoints:**
- **Production:** `https://ipgpayment.payable.lk/ipg/pro/refund-status`
- **Sandbox:** `https://sandboxipgpayment.payable.lk/ipg/sandbox/refund-status`
- **QA:** `https://payable-ipg-qa.web.app/ipg/qa/refund-status`
- **Dev:** `https://payable-ipg-dev.web.app/ipg/dev/refund-status`

**Request:** `POST` with JSON body:
```json
{
  "orderId": "your-order-id"
}
```

**Response:** Refund notification data.

**Example:**
```
{
    "status": 200,
    "data": {
        "payableOriginalTxId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        "payableOriginalOrderId": "oid-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        "payableRefundTxId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        "refundedDateTime": "2026-06-25 13:17:40.0",
        "refundedAmount": "19.99",
        "totalRefundedAmount": "19.99",
        "checkValue": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    }
}
```
