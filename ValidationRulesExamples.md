# Salesforce Validation Rules Examples

## Account Validation Rules

### Rule 1: Annual Revenue Required for Certain Industries
**Error Condition Formula:**
```
AND(
    OR(Industry='Technology', Industry='Finance'),
    ISBLANK(AnnualRevenue)
)
```

### Rule 2: Credit Limit for New Accounts
**Error Condition Formula:**
```
AND(
    CreatedDate = TODAY(),
    CreditLimit__c > 1000000
)
```

## Opportunity Validation Rules

### Rule 3: Discount Limit
**Error Condition Formula:**
```
Discount__c > 0.25
```

### Rule 4: Close Date must be in Future
**Error Condition Formula:**
```
CloseDate <= TODAY()
```

## Contact Validation Rules

### Rule 5: Email or Phone Required
**Error Condition Formula:**
```
AND(
    ISBLANK(Email),
    ISBLANK(Phone)
)
```
