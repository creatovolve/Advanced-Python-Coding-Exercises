

---

## 📄 `abcs.md`

```markdown
# Abstract Base Classes (ABCs)

## Topic
Abstract Base Classes as validated duck typing.  
(Fluent Python – Chapters 11 & 12)

---

## Motivation
Pure duck typing fails late at runtime. ABCs validate required behavior early.

---

## Problem Scenario
A payment system accepts multiple gateways; each must implement `pay(amount)`.

---

## Code Example

```python
from abc import ABC, abstractmethod

class PaymentGateway(ABC):
    @abstractmethod
    def pay(self, amount):
        pass

class UpiGateway(PaymentGateway):
    def pay(self, amount):
        print("Paid", amount)
