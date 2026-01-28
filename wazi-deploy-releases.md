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




The following table provides a detailed overview of the **IBM Wazi Deploy** release history and key features from late 2023 through August 2025, based on the provided sources. 

Please note that the sources currently only provide information up to **August 2025**; there is no data available for scheduled releases in **2026**.

### IBM Wazi Deploy Release Summary (2023–2025)

| Version | Release Date | Key Features and Improvements |
| :--- | :--- | :--- |
| **3.0.6.1** | *Post-3.0.6* | **Interim fix** recommended for immediate application for all 3.0.6 users. |
| **3.0.6** | 2025 (Estimated) | Root-level **`rescue`** instructions; **`beginAt`** argument to start deployments at specific steps; custom **Jinja2 filters** for Python; new **`sequential_restore`** and **`uss_restore`** building blocks. |
| **3.0.5.2** | August 2025 | Performance fixes for **`USE_NATIVE_COPY`**; fix for **`DB2_BIND_PACKAGE`** exceptions when routing to secondary machines; **`force_lock`** support for Python. |
| **3.0.5.1** | July 2025 | Addressed slower performance in deployment steps when using native copy options. |
| **3.0.5** | 2025 | **YAML schemas** for configuration validation; new **GDG management** building blocks (`gdg_archive`, `gdg_copy`, etc.); **`ims_ddl`** building block for SQL submissions. |
| **3.0.4** | February 2025 | **`http_request`** building block for REST APIs; **pre-deployment checks** to block failing triggers; **initial `rescue`** instruction; fixed SSL errors for CICS. |
| **3.0.3** | October 2024 | **Simplified offline installation** (all requisites included); **local packaging** via `wazideploy-package`; **conditional deployment** (`loop`, `when`, `failed_when`, `jumps_when`). |
| **3.0.2** | March/May 2024 | Support for **Linux x86 and Linux on Z** for Ansible; new **`tso_command`** and **`ims_olcutl`** building blocks; artifact renaming support. |
| **3.0.1** | October 2023 | Introduction of the **Evidence Requester** for auditing; support for **IMS applications** and **Nexus** artifact repositories. |

---

### Key Technical Takeaways for your MVP

*   **Architecture:** Wazi Deploy remains a **serverless** tool, constituted solely of a **Command-Line Interface (CLI)**, which makes it highly compatible with CI/CD pipelines like Jenkins or GitLab.
*   **Deployment Logic:** Recent 2025 updates (3.0.4–3.0.6) heavily emphasize **error handling** through the `rescue` instruction and **flexibility** with the `beginAt` argument, allowing you to resume failed deployments from a specific point.
*   **Performance:** Version 3.0.5 and 3.0.6 introduced significant performance enhancements for the **`use_native_copy`** variable, which uses the native UNIX `cp` command instead of ZOAU to speed up file transfers.
*   **Validation:** For a robust student or customer playground, the **YAML schemas** introduced in version 3.0.5 allow for automated validation of deployment methods and manifest files before execution.

Would you like more details on the specific **Python environment variables** or **SMP/E installation steps** required for the latest 3.0.5/3.0.6 versions?
