
# 💡 Monitor Fabric Activity using the Monitoring Hub

This lab walks you through the process of monitoring activity in Microsoft Fabric using the **Monitoring Hub**, along with creating and working with a **Lakehouse**, **Dataflow Gen2**, and **Spark Notebooks**.

🕒 **Estimated Duration**: 30 minutes  
🛠 **Requirements**: Access to a Microsoft Fabric tenant with Fabric capacity enabled (Trial, Premium, or Fabric)

---

## 📁 1. Create a Workspace

1. Go to [Microsoft Fabric Home](https://app.fabric.microsoft.com/home?experience=fabric-developer).
2. From the sidebar, click **Workspaces**.
3. Create a new workspace.
   - Name it as desired.
   - Choose a **licensing mode** that includes **Fabric capacity**.

---

## 🌊 2. Create a Lakehouse

1. In the workspace, click **Create** → **Lakehouse**.
2. Assign a name to your new lakehouse.
3. After creation, open the lakehouse. It will initially be empty.

---

## 🔁 3. Create and Monitor a Dataflow Gen2

1. In your lakehouse’s Home page, go to **Get data** → **New Dataflow Gen2**.
2. Name it: `Get Product Data` → Click **Create**.
3. In the dataflow designer:
   - Choose **Import from a Text/CSV file**.
   - Use the following URL:  
     `https://raw.githubusercontent.com/MicrosoftLearning/dp-data/main/products.csv`
   - Use **Anonymous authentication**.
4. Review the data preview.
5. **Publish** the dataflow.
6. Go to the **Monitor** tab from the sidebar to check its status.
7. Once completed, return to the lakehouse and check the **Tables** section.
   - A table named `products` should appear.

---

## 📓 4. Create and Monitor a Spark Notebook

1. Click **Create** → **Notebook** under Data Engineering.
2. Rename notebook to `Query Products`.
3. In the **Explorer pane**, add your lakehouse as a data source.
4. Navigate to the `products` table.
5. Click `...` → **Load data > Spark** to auto-generate a Spark read query.
6. Click **Run all** to execute the notebook.
7. Once results load, click **Stop session** to release resources.
8. Go to **Monitor** to see notebook activity logs.

---

## 📜 5. Monitor History for an Item

1. Return to your workspace and click **Refresh now** on the `Get Product Data` dataflow.
2. Go to **Monitor**.
3. Under the `...` menu of the dataflow, select **Historical runs**.
4. Use **View detail** to see execution specifics.
5. Use **Back to main view** to return.

---

## 🧩 6. Customize Monitoring Hub Views

1. In the Monitoring Hub:
   - Click **Filter**.
     - Status: `Succeeded`
     - Item type: `Dataflow Gen2`
2. Click **Column Options** and enable:
   - Activity name
   - Status
   - Item type
   - Start time
   - Submitted by
   - Location
   - End time
   - Duration
   - Refresh type

---

## 🧹 7. Clean Up Resources

1. Go to your workspace.
2. Click `...` → **Workspace settings**.
3. In the **General** section, click **Remove this workspace** to delete all resources.

---

## ✅ Summary

By the end of this lab, you have:
- Created and managed a Lakehouse
- Built a Dataflow Gen2 to ingest CSV data
- Queried data using Spark Notebooks
- Monitored execution status through the Monitoring Hub

---

## 📎 Resources

- [Microsoft Fabric Documentation](https://learn.microsoft.com/fabric)
- [Fabric Dataflows](https://learn.microsoft.com/fabric/data-engineering/dataflows)
- [Lakehouse in Fabric](https://learn.microsoft.com/fabric/data-engineering/lakehouse-overview)

---

> 🧠 Tip: Fabric is an evolving platform. Always check for the latest updates and feature releases via the Microsoft Learn documentation.
