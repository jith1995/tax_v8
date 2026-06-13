# CA Review Notes

This is a review/demo MVP. Please validate all tax logic before public use.

## Areas needing detailed review

- ITR form eligibility edge cases
- Old vs new regime deductions and exceptions
- 87A rebate treatment by income type and special-rate income
- Capital gains: equity, equity MF, debt MF, property, gold, ESOP/RSU, VDA, loss set-off, grandfathering/indexation/exemptions
- NRI day-count, DTAA, NRE/NRO treatment and TDS
- House property self-occupied vs let-out, co-ownership and home-loan interest restrictions

## Latest CA feedback update - Income-head-wise deductions

Updated the Tax Path Check MVP to separate income-head computation before common deductions:

- Salary now captures gross salary and professional tax separately.
- House property / rental now captures gross annual rent, municipal taxes actually paid, and home-loan interest on rented property.
- House property preview computes: gross rent minus municipal taxes = net annual value; less 30% standard deduction; less interest on borrowed capital = taxable house property income.
- FD / bank interest is now under Income from Other Sources, not Capital Gains.
- Common deductions are kept separate in Step 4 after income-head computation.
- Review now shows an income-head-wise breakdown before old/new regime tax calculation.

CA review pending items:
- Final treatment of house property loss set-off and carry forward.
- New regime treatment for house property interest and loss set-off.
- HRA and 80GG eligibility logic.
- Professional tax treatment across regimes and state-wise limits.
- Capital gains detailed set-off rules and Schedule CG validation.


## Latest UX structure

The detailed Tax Path Check is now on `tax-tool.html`, separate from the homepage. The homepage remains a preview and content/SEO landing page.
