# Prompting Styles Analysis

## Accuracy Comparison
| Prompt Style | Accuracy (%) |
| :--- | :--- |
| Zero-Shot | 73.333% |
| Few-Shot | 73.333% |
| Role-Based | 73.333% |

---

## Performance Breakdown

### 3 Examples Where Each Style Won
1. **Zero-Shot:** Ticket #[2] - "[Could you tell me where my package currently is? Tracking hasn't updated in three days.]" -> Correctly predicted `[Shipping]`.
2. **Few-Shot:** Ticket #[4] - "[I noticed a double charge on my credit card statement for my latest subscription payment]" -> Correctly predicted `[Payment]`.
3. **Role-Based:** Ticket #[10] - "[My tracking link says my parcel was delivered, but there’s nothing at my front door.]" -> Correctly predicted `[Shipping]`.

### 3 Examples Where Each Style Failed
1. **Zero-Shot:** Ticket #[12] - Predicted `[Login]`, Ground Truth was `[Other]`.
2. **Few-Shot:** Ticket #[13] - Predicted `[Other]`, Ground Truth was `[Payment]`.
3. **Role-Based:** Ticket #[14] - Predicted `[Account]`, Ground Truth was `[Refund]`.

---

## Conclusion & Recommendations
* **Zero-Shot:** Best for simple, unambiguous classification tasks where speed and minimal prompt length are prioritized.
* **Few-Shot:** Best for nuanced categories or strict formatting needs where providing example patterns helps guide the model.
* **Role-Based:** Best for complex decision-making where tone, intent, or domain-specific context matters.