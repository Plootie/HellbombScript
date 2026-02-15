## Security Info:

EXE [VirusTotal](https://www.virustotal.com/gui/file/B6B28FF0D96788371087DDE8F1BAF463F4FA7945F624C44638923F59AF5B2B5C) & [Hybrid Analysis](https://www.hybrid-analysis.com/sample/B6B28FF0D96788371087DDE8F1BAF463F4FA7945F624C44638923F59AF5B2B5C) link.

Not sure you trust the EXE? You can run
```powershell
"Hellbomb_Script_v4.0-5c36c40.exe" -extract:$env:USERPROFILE"\Downloads\Hellbomb Script.ps1"
```
in PowerShell to extract the script from the EXE to verify it's the same source code as what's shown here.

**Script Version** [VirusTotal Results](https://www.virustotal.com/gui/file/3A67E62924B40BADF4A88CF0E7BE0BD6F9654C8876B21AE7532FAEECD10BC77F)

The ``Hellbomb Script.ps1`` SHA256 hash should match the VirusTotal file hash of ``3A67E62924B40BADF4A88CF0E7BE0BD6F9654C8876B21AE7532FAEECD10BC77F``.

**Script Version** [Hybrid-Analysis Link](https://www.hybrid-analysis.com/sample/3A67E62924B40BADF4A88CF0E7BE0BD6F9654C8876B21AE7532FAEECD10BC77F)

You can compare the file hash to the VirusTotal link to ensure that the VirusTotal results match the file you're attempting to run.

1. Download [the latest release](https://github.com/helldivers2fixes/HellbombScript/releases/latest) by clicking on Source Code.zip. Drill down into the folders and extract Hellbomb Script.ps1
2. In Terminal or PowerShell ``cd`` (Change to the directory) where the script is saved
3. If you downloaded the .ps1 file to your Downloads folder, run
```powershell
cd $((New-Object -ComObject Shell.Application).Namespace('shell:Downloads').Self.Path)
```
4. Run
```powershell
Get-FileHash 'Hellbomb Script.ps1' -eq 3A67E62924B40BADF4A88CF0E7BE0BD6F9654C8876B21AE7532FAEECD10BC77F
```
5. The statement should return/evaluate to ``True``

## Why does it need Admin Privileges?
- Reads firewall rules
- Installs Microsoft Visual C++ redistributables
- Downloads and runs the zip file version of [CPU-Z](https://www.cpuid.com/softwares/cpu-z.html) from CPUID
