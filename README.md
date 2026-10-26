# ProFabX website

`web/` contains the built public website: home, quote workbench, CMF, partners and about pages. Relative asset URLs support a GitHub Pages repository subpath.

## Deployment

Configure repository Settings → Pages → Source as GitHub Actions. Pushing the default branch (main or master) or dispatching the Publish ProFabX website workflow publishes only `web/`.

## Public and local capabilities

Model imports, placement, quote calculations, local browser storage, materials and transaction downloads run in the browser. GitHub Pages is a static host: native Bambu/Creality slicing, real-time desktop synchronization and native support generation require the separate local ProFabX preview service. No native executables, user models/orders, login profiles, runtime descriptors or engineering backups are included here.

## Updates

Build the local website with the existing Vite project, then replace `web/` with its `dist/` output while preserving `.nojekyll`. The engineering source and native toolchain remain in the local project.

## Pricing standards (2026-10-26)

The quote workbench now displays 26 process/material standards and two opt-in project schedules (Handle 20260302 and Truffle). Sample/batch production is selected explicitly. Within each process/material group, manufacturing cost is the maximum of total gram charges, aggregate per-piece minimums and the order minimum. Finishing/setup are additional, then the existing discount-before-tax calculation applies.

Ranged rates require selection within the supplied interval. Project/difficulty-only and unsupported material prices require explicit manual input. Risk-floating prices carry review labels; no difficulty multiplier is fabricated. Gram charges round each row total to cents. PAT10 transparent treatment optionally adds 3 yuan/g. Weight is entered or explicitly labelled as a geometric estimate. Historical quotes retain prior manual prices until the user adopts standards. Exported Excel/print quotes include the applied basis and minimum top-up.

### 报价合同模板
- 按提供的黑白A4模板生成报价单，可编辑客户、联系人、交期、付款方式和备注。
- 明细显示单件重量与元/g报价标准，注明估重及人工核价；支持零件图片、Excel下载和打印/另存PDF。
- 原报价标准、起步补差、折扣与税额逻辑保持一致，多页PDF自动重复表头。
