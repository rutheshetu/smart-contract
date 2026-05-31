---
marp: true
---

# Structs

- 🧺 group variables under a single name
- 💿 can be stored in the different data locations
- 🪆 can go within other structs/arrays/mappings

Example:

struct User {
  bool isActive;
  uint balance;
}

User user = User(true, 0);
---

## Grouping Variables

contract Escrow {
    struct Agreement {
      address depositor;
      address beneficiary;
      address arbiter;
      uint paymentAmount;
    }
    Agreement agreement;

    constructor(Agreement memory _agreement) {
      agreement = _agreement;
    }
}
---

## Modeling Data

contract X {
    enum OrderStatus { Created, Paid, Shipped, Completed }

    struct Order {
        address buyer;
        address seller;
        uint256 amount;
        OrderStatus status;
    }

    Order[] orders;
}
