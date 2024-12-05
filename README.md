# MayaPymelTroubleshooting

## Fixing "No module named 'pymel'" in Autodesk Maya

This guide will help you resolve the "No module named 'pymel'" error in Autodesk Maya when using Python scripts such as **Spring Magic 3.5a Python 3**. This issue commonly occurs in Maya 2022 or newer versions, which use Python 3. Follow the steps below to troubleshoot and fix the issue.

---

## Quick Steps

1. **Open Command Prompt**:
   - Press `Win + R`, type `cmd`, and hit `Enter`.

2. **Navigate to Maya's `bin` Directory**:
   ```bash
   cd "C:\Program Files\Autodesk\Maya2023\bin"
   ```

3. **Check if `pymel` is Installed**:
   - Run the following command to list installed Python packages:
     ```bash
     mayapy -m pip list
     ```

4. **Update `pip`**:
   - Upgrade `pip` to the latest version:
     ```bash
     mayapy -m pip install --upgrade pip
     ```

5. **Install or Update `pymel`**:
   - Use the following command to install or update `pymel`:
     ```bash
     mayapy -m pip install pymel --upgrade
     ```

6. **Restart Maya**:
   - Close and reopen Maya to apply the changes.

---

## Why This Error Happens
The error occurs when attempting to install and use **Spring Magic 3.5a Python 3** in Maya 2022 or newer versions, which apply Python 3. This script relies on the `pymel` module, which may not be pre-installed in your environment, leading to the "No module named 'pymel'" error.

For more information about Spring Magic, visit the official website: [Spring Magic on AnimBai](https://animbai.com/2017/10/28/spring-magic/).

---

## Video Tutorial
For a step-by-step walkthrough, watch this YouTube tutorial: [Fix "No module named 'pymel'" Error in Maya](https://youtu.be/uOn_EUFJnSU)

---

## Notes
- Ensure you're using the correct Maya version's `mayapy` when navigating to the `bin` directory.
- After completing these steps, try running your script again, e.g.:
  ```python
  import springmagic
  springmagic.main()
  ```
