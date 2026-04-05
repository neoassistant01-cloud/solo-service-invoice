# Solo Service Invoice - Data Model

## Entities

### Business
```json
{
  "id": "business-1",
  "name": "ABC Plumbing",
  "address": "123 Main St",
  "phone": "555-1234",
  "createdAt": "2026-04-04T00:00:00Z"
}
```

### Customer
```json
{
  "id": "cust-uuid",
  "name": "John Smith",
  "address": "456 Oak Ave",
  "phone": "555-5678",
  "createdAt": "2026-04-04T00:00:00Z"
}
```

### Invoice
```json
{
  "id": "inv-uuid",
  "invoiceNumber": "INV-001",
  "date": "2026-04-04",
  "customer": { "id", "name", "address" },
  "serviceDescription": "Fix leaky faucet",
  "lineItems": [
    { "service": "Labor", "quantity": 1, "rate": 150 }
  ],
  "subtotal": 150,
  "tax": 0,
  "total": 150,
  "status": "created",
  "createdAt": "2026-04-04T00:00:00Z"
}
```

### LineItem
```json
{
  "service": "Service name",
  "quantity": 1,
  "rate": 150
}
```

## Storage
- **localStorage** for browser-based persistence
- Keys: `ssi_business`, `ssi_customers`, `ssi_invoices`
- JSON serialized

## Data Constraints
- Invoice number: auto-increment, format INV-XXX
- No duplicate customer names (提示)
- Line items: min 1 required
