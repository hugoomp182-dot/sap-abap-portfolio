# SAP ABAP Portfolio – Hotel Management Projects

**Author:** Hugo O. M. P.  
**Certification:** SAP Certified Associate – Back-End Developer (ABAP Cloud)  
**Environment:** SAP BTP ABAP Environment (Trial) | Eclipse ADT  

---

## About This Portfolio

I work in purchasing and accounting at a hotel. These projects are based on real operational workflows I manage daily, built to demonstrate SAP ABAP development skills for junior/associate consultant roles.

---

## Project 1 – Supplier Invoice & Payment Order Manager (FI / RAP)

### Business Context
In a hotel, every department (kitchen, restaurant, housekeeping, maintenance) generates purchase invoices from suppliers. The accounting team must track each invoice, validate it, and generate a Payment Order (OP) before marking it as paid. This project digitizes and automates that process.

### Technical Stack
- SAP RAP (Restful ABAP Programming Model)
- Core Data Services (CDS) – Interface View + Projection View
- Fiori Elements (List Report)
- OData V4
- SAP BTP ABAP Environment

### Artifacts Created
| Artifact | Name | Description |
|---|---|---|
| Database Table | `ZFACTURA_PROV` | Stores supplier invoices |
| CDS Interface View | `ZI_FacturaProv` | Root view entity |
| CDS Projection View | `ZC_FacturaProv` | Fiori UI annotations |
| Behavior Definition | `ZI_FACTURAPROV` | Managed, with validations |
| Behavior Definition | `ZC_FACTURAPROV` | Projection with create/update/delete |
| Behavior Implementation | `ZBP_I_FACTURAPROV` | Business logic handler |
| Service Definition | `ZUI_FACTURAPROV` | Exposes entity |
| Service Binding | `ZUI_FACTURAPROV_O4` | OData V4, published |

### Business Logic Implemented
- **validarMonto** – Rejects invoices with amount ≤ 0
- **validarPagoConOP** – Prevents marking an invoice as "Paid" without a Payment Order number
- **calcularVencida** – Automatically sets status to "Overdue" when due date has passed

### App Screenshot
![Fiori Elements Preview](SAP%20FIORI.png)

---

## Project 2 – Goods Receipt & Stock Management (MM / Classic ABAP)
*Coming soon*

---

## Project 3 – Purchasing & Payments Integration
*Coming soon*
