🧩 Skeleton Loader Task 
JUST DO THIS FIRST (Don’t Read Below Yet)
1️⃣ Work ONLY on these files (in this order)
🟢 Batch 1 (Start here)

src/pages/PolicyHolder/DailyEventsSection.js
→ Replace page <CircularProgress /> with TableSkeleton

src/pages/PaymentSubscriber/index.js
→ Replace page <CircularProgress /> with TableSkeleton or CardSkeleton

src/pages/ClaimSettlement/ClaimSettlementTable.js
→ Improve / verify existing row skeleton loading

🟡 Batch 2 (Only after Batch 1 is merged)

src/pages/Payments/index.js
→ Replace page <CircularProgress /> with TableSkeleton or CardSkeleton

src/pages/DeviceManagment/index.js
→ Review only (mostly button loader, likely no change)

src/pages/ClaimSettlement/PolicyHolderClaimDetails.jsx
→ Replace page loader with CardSkeleton or FormSkeleton

🔴 Batch 3 (Do last)

src/pages/AssetManagment/AssetDetails.js
→ Replace page loader with ProfileSkeleton

src/pages/WorkOrders/AppIssue.js
→ Replace list loader with ListItemSkeleton

2️⃣ What to replace (simple rule)

If you see this:

{loading ? <CircularProgress /> : <Content />}


Replace it with a skeleton, not a spinner.

3️⃣ How to replace it
// BEFORE
{loading ? <CircularProgress /> : <Content />}

// AFTER
{loading ? <TableSkeleton /> : <Content />}

📘 READ BELOW ONLY IF NEEDED
🚫 DO NOT TOUCH THESE
❌ Already Done (Skeletons Exist)

Do NOT edit anything in:

src/pages/Analytics/
src/pages/Notification/
src/pages/Setting/SettingsPage.js
src/pages/Firmwares/index.js
src/pages/UserManagment/index.js
src/pages/TripsManagement/index.js
src/pages/UpdateHistory/
src/pages/ServiceRequest/
src/pages/SubAccount/
src/pages/PolicyHolder/index.js
src/pages/Geofencing/GeofenceTable.js
src/pages/Authority/index.js
src/pages/UnhandledOrders/index.js
src/pages/SubscriberManagment/
src/pages/AssetType/index.js
src/pages/AssetManagment/index.js
src/pages/DeviceManagment/index.js (table)
src/pages/FleetManagment/FleetTable.js
src/pages/Firmware/DeviceTable.js
src/pages/Firmware/FirmwareTable.js
src/pages/Firmware/FirmwareDetailsModal.js
src/pages/WorkOrders/IssueTypes.js
src/pages/Dashboard/TrackOrder.js
src/pages/AssetManagment/AssetDetailsCopy.js
src/pages/AssetType/AddEditAssetType.js

❌ Do NOT Replace These Loaders

These are correct and must stay:

CircularProgress inside buttons

Autocomplete dropdown loaders

Battery / circular progress UI

Text loaders like "Saving...", "Creating..."

🧱 Skeleton Imports
Table pages
import TableSkeleton from '../../components/TableSkeleton';

Non-table pages
import {
  CardSkeleton,
  ProfileSkeleton,
  ListItemSkeleton,
  FormSkeleton,
} from '../../components/ui/Skeleton/Skeleton';

🧠 Skeleton Selection Rule
UI	Skeleton
Table	TableSkeleton
Cards	CardSkeleton
Form	FormSkeleton
Profile / Details	ProfileSkeleton
List	ListItemSkeleton
🧪 Testing (Mandatory)

Open DevTools → Network

Select Slow 3G

Reload page

You should see:

Skeletons (not spinner)

No layout jump

Content loads correctly

✅ Final Checklist

 Only assigned files changed

 Skip files untouched

 Correct skeleton used

 Button loaders untouched

 Tested on Slow 3G

 No console errors

🆘 If Stuck

Check Firmwares/index.js for example

Read comments in Skeleton.jsx

Ask Me(Ajay)
