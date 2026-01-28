Based on the provided sources, the releases for IBM Wazi Deploy in **2025** include versions **3.0.4, 3.0.5, and 3.0.6**. There is currently **no information regarding releases for 2026** in the provided documents, as the latest updates only cover up to August 2025.

### **List of IBM Wazi Deploy Releases in 2025**

The following table summarizes the documented releases and interim fixes for the year 2025:

| Version / Fix | Release Month | Key Highlights | Source |
| :--- | :--- | :--- | :--- |
| **3.0.4** | February 2025 | Fixed SSL errors when deploying to CICS using the Python translator. | |
| **3.0.4 (Interim Fix)**| June 2025 | Addressed a failure in the `member_archive` step during first-time deployments. | |
| **3.0.5.1 (PTF)** | July 2025 | Performance improvements for `USE_NATIVE_COPY` and DB2 bind exceptions. | |
| **3.0.5.2 (PTF)** | August 2025 | Further updates to native copy and `force_lock` variables for Python deployments. | |
| **3.0.6** | Not Specified* | Introduced **rescue** instructions at the root level and the **beginAt** argument. | |
| **3.0.6.1 (Interim Fix)**| Not Specified* | Recommended for immediate application for all users of version 3.0.6. | |

*\*Note: While version 3.0.6 is listed in the "What's new" section of the sources alongside the 2025 updates, a specific release month is not explicitly cited for the 3.0.6 baseline.*

---

### **Key Features Introduced in 2025 Releases**

*   **Version 3.0.6 Enhancements:** This version introduced the ability to specify a **`beginAt` argument** on the deployment command, allowing users to start a deployment at a specific activity, action, or step. It also allowed for custom **Jinja2 filters** in Python deployments.
*   **Version 3.0.5 Enhancements:** This release added **YAML schemas** to validate the structure of configuration and manifest files. It also introduced several new building blocks for managing **Generation Data Group (GDG)** files, such as `gdg_archive` and `gdg_copy`.
*   **Performance Improvements:** Throughout 2025, updates focused on optimizing the **`use_native_copy`** option to speed up copy operations in `member_archive`, `member_copy`, and `member_restore` building blocks.
*   **Deployment Controls:** Version 3.0.4 introduced **automatic checks** that run before a deployment starts; if these controls fail, the deployment is not triggered.

### **Information Regarding 2026**
The sources provided are current only through **August 19, 2025**. Therefore, they **do not contain a roadmap or a list of releases for 2026**.

**Would you like to know more about the specific technical requirements for the latest 3.0.6 release, such as the supported Python or ZOAU versions?**
