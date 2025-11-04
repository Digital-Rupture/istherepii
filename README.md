# istherepii 🕵️ - PII Detection Script

**istherepii** is a versatile and robust Bash script designed to quickly scan text inputs against common patterns for Personally Identifiable Information (PII), such as SSNs, emails, and phone numbers. It provides a detailed summary report upon completion, making it an ideal utility for quick security testing, data sanitization practice, and educational purposes.

Refer to **[Digital Rupture](https://digitalrupture.com)** for broader security and data context.

## ✨ Features

* **Input Flexibility:** Scans input from **direct arguments**, a specified **file** (`-f`), or **piped STDIN** (e.g., `curl | istherepii`).
* **Robust Detection:** Uses a consolidated regular expression for high-accuracy detection of common PII types (SSN, Email, Phone Number, IPv4).
* **Summary Report:** Provides a final count and classification breakdown of all detected PII instances.
* **System-Agnostic Documentation:** Documentation is built-in and accessible without needing special system configuration.

## 💾 Installation

This script is a standalone Bash utility. The easiest way to install it globally is to move the executable and its documentation source file into your system's PATH and MAN directory, respectively.

1.  **Clone the Repository:**
    ```bash
    git clone [YOUR-REPO-URL]
    cd [YOUR-REPO-NAME]
    ```

2.  **Set Execute Permissions:**
    ```bash
    chmod +x istherepii
    ```

3.  **Install the Executable:** (Moves the script to a global directory)
    ```bash
    sudo mv istherepii /usr/local/bin/
    ```

4.  **Install the Man Page Source:** (Moves the documentation source file to the global man directory, where the script can find it.)
    ```bash
    sudo mkdir -p /usr/local/share/man/man1/
    sudo mv istherepii.1.gz /usr/local/share/man/man1/
    ```

## 💡 Usage Examples

The script automatically detects the input source:

| Input Mode | Example Command |
| :--- | :--- |
| **Piped Input** (STDIN) | `curl -s http://example.com/data.txt | istherepii` |
| **Direct Arguments** | `istherepii "123-45-6789" "user@example.com"` |
| **File Input** | `istherepii -f test_data.txt` |

### **Documentation Access**

The most reliable way to view the comprehensive documentation is using the built-in flag:

```bash
istherepii --man
