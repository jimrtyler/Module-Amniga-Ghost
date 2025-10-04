# 👻 Modulka Amniga Ghost
**Qalab Xoojinta Amniga Windows iyo Azure oo ku salaysan PowerShell**

> **Xoojinta amniga firfircoon ee Windows endpoints iyo deegaannada Azure.** Ghost wuxuu bixiyaa shaqooyinka xoojinta ku salaysan PowerShell kuwaas oo kaa caawin kara in ay dhimaan waddooyinka weerarka caadiga ah iyagoo damiyaan adeegyada iyo borotokoolada aan loo baahnin.

## ⚠️ Digniin Muhiim ah

**TIJAABO WAA IN LA SAMEEYAA**: Had iyo jeer marka hore ku tijaabow Ghost gudaha deegaannada aan wax soosaarta ahayn. Daminta adeegyada waxay saameyn kartaa hawlaha ganacsiga xalaalka ah.

**DAMAANAD MA LEH**: In kastoo Ghost uu bartilmaameedsado waddooyinka weerarka caadiga ah, ma jiro qalab amni ah oo ka hortagin kara dhammaan weerarrada. Tani waa hal curiye dhexe ah istiraatiijiyada amniga oo dhamaystiran.

**SAAMAYNTA HAWLGELINTA**: Qaar ka mid ah shaqooyinku waxay saameyn karaan hawlgalka nidaamka. Si taxaddar leh u dib u eeg goob kasta ka hor inta aan la geynin.

**QIIMAYN XIRFADEED**: Deegaanno wax soo saarista ah, kala tashi xubnaaha amniga si loo hubiyo in goobaha ay ku habboon yihiin baahiyaha hay'addaada.

## 📊 Muuqaalka Amniga

Waxyeelada Ransomware waxay gaartay **$57 bilyan 2025**, cilmi-baadhis muujinaya in weerar badan oo guul leh ay u adeegsadaan adeegyada aasaasiga ah ee Windows iyo qaabeynta khaldan. Waddooyinka weerarka caadiga ah waxaa ka mid ah:

- **90% dhacdooyinka ransomware** waxaa ku jira RDP-ga la faa'iidaysto
- **Nugulka SMBv1** ayaa awood u siiyay weerarro sida WannaCry iyo NotPetya
- **Faylasha shuruudaha** waxay sii ahaan yihiin habka aasaasiga ah ee soo gudbinta malware-ka
- **Weerarrada USB-ku salaysan** waxay sii wadaan in ay bartilmaameedsadaan shabakadaha hawada-godka ah
- **Si xun u isticmaalka PowerShell** wuu si weyn u kordiyay sannadihii u dambeeyay

## 🛡️ Shaqooyinka Amniga Ghost

Ghost wuxuu bixiyaa **16 shaqooyinka xoojinta Windows** iyo **isdhexgalka amniga Azure**:

### Xoojinta Windows Endpoint

| Shaqada | Ujeeddo | Tixraacyo |
|----------|---------|----------------|
| `Set-RDP` | Waxay maamusho gelitaanka Remote Desktop | Waxay saameyn kartaa maamulka fog |
| `Set-SMBv1` | Waxay kontoroolaysaa borotokoolka SMB ee duugan | Loo baahan yahay nidaamyo aad u duug ah |
| `Set-AutoRun` | Waxay xakameysaa AutoPlay/AutoRun | Waxay saameyn kartaa raaxada isticmaalaha |
| `Set-USBStorage` | Waxay xaddidaysaa qalabka kaydka USB | Waxay saameyn kartaa isticmaalka xalaalka ah ee USB |
| `Set-Macros` | Waxay xakameysaa fulinta makrooska Office | Waxay saameyn kartaa dukumentiyada makroo la hawl-geliyay |
| `Set-PSRemoting` | Waxay maamusho PowerShell fog | Waxay saameyn kartaa maamulka fog |
| `Set-WinRM` | Waxay xakameysaa Windows Remote Management | Waxay saameyn kartaa maamulka fog |
| `Set-LLMNR` | Waxay maamusho borotokoolka xallinta magacyada | Caadi ahaan waa amaan in la damiyey |
| `Set-NetBIOS` | Waxay xakameysaa NetBIOS ee TCP/IP | Waxay saameyn kartaa codsiyada duugan |
| `Set-AdminShares` | Waxay maamusho wadaagga maamulka | Waxay saameyn kartaa gelitaanka faylasha fog |
| `Set-Telemetry` | Waxay xakameysaa ururinta xogta | Waxay saameyn kartaa awood baadhista |
| `Set-GuestAccount` | Waxay maamusho akoonka martida | Caadi ahaan waa amaan in la damiyey |
| `Set-ICMP` | Waxay xakameysaa jawaabaha ping | Waxay saameyn kartaa baadhista shabakada |
| `Set-RemoteAssistance` | Waxay maamusho Remote Assistance | Waxay saameyn kartaa hawlgallada caawinta |
| `Set-NetworkDiscovery` | Waxay xakameysaa helitaanka shabakada | Waxay saameyn kartaa daabacaadda shabakada |
| `Set-Firewall` | Waxay maamusho Windows Firewall | Muhiim u ah amniga shabakada |

### Amniga Daruurta Azure

| Shaqada | Ujeeddo | Shuruudaha |
|----------|---------|--------------|
| `Set-AzureSecurityDefaults` | Waxay awood siisaa amniga aasaasiga ah ee Azure AD | Fasaxaadka Microsoft Graph |
| `Set-AzureConditionalAccess` | Waxay qaabeysaa siyaasadaha gelitaanka | Shatiyeynta Azure AD P1/P2 |
| `Set-AzurePrivilegedUsers` | Waxay soo baadhaa akoonadka mudanayaasha ah | Fasaxaadka Global Admin |

### Ikhtiyaarrada Geynta Ganacsi

| Habka | Kiiska Isticmaalka | Shuruudaha |
|--------|----------|--------------|
| **Fulinta Toos ah** | Tijaabin, deegaanno yaryar | Xuquuqda maamule maxalli ah |
| **Group Policy** | Deegaannada domain | Maamulaha domain, maareynta GP |
| **Microsoft Intune** | Qalabka daruurta la maareeyay | Shatiyeynta Intune, Graph API |

## 🚀 Bilow Degdeg ah

### Qiimaynta Amniga
```powershell
# Soo daji modulka Ghost
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')

# Hubi amniga hadda jira
Get-Ghost
```

### Xoojinta Aasaasiga ah (Marka Hore Tijaabow)
```powershell
# Xoojinta muhiimka ah - marka hore ku tijaabow deegaanka shaybaarka
Set-Ghost -SMBv1 -AutoRun -Macros

# Dib u eeg isbeddellada
Get-Ghost
```

### Geynta Ganacsi
```powershell
# Geynta Group Policy (deegaannada domain)
Set-Ghost -SMBv1 -AutoRun -GroupPolicy

# Geynta Intune (qalabka daruurta la maareeyay)
Set-Ghost -SMBv1 -RDP -USBStorage -Intune
```

## 📋 Hababka Rakibista

### Ikhtiyaarka 1: Soo dejinta Toos ah (Tijaabin)
```powershell
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')
```

### Ikhtiyaarka 2: Rakibista Modulka
```powershell
# Ka rakib PowerShell Gallery (marka la heli karo)
Install-Module Ghost -Scope CurrentUser
Import-Module Ghost
```

### Ikhtiyaarka 3: Geynta Ganacsi
```powershell
# U koobiyee meel shabakad geynta Group Policy
# Qaabeey qoraalada PowerShell ee Intune geynta daruurta
```

## 💼 Tusaalayaasha Kiisaska Isticmaalka

### Ganacsi Yar
```powershell
# Ilaalinta aasaasiga ah oo aan saameyn yar lahayn
Set-Ghost -SMBv1 -AutoRun -Macros -ICMP
```

### Deegaanka Daryeelka Caafimaadka
```powershell
# Xoojinta diiradda saareysa HIPAA
Set-Ghost -SMBv1 -RDP -USBStorage -AdminShares -Telemetry
```

### Adeegyada Maaliyadda
```powershell
# Qaabeynta amniga sare
Set-Ghost -RDP -SMBv1 -AutoRun -USBStorage -Macros -PSRemoting -AdminShares
```

### Hay'adda Cloud-First
```powershell
# Geynta Intune-maareeyay
Connect-IntuneGhost -Interactive
Set-Ghost -SMBv1 -RDP -AutoRun -Macros -Intune
```

## 🔍 Faahfaahinta Shaqooyinka

### Shaqooyinka Xoojinta Asaasiga ah

#### Adeegyada Shabakada
- **RDP**: Waxay xidhataa gelitaanka desktop fog ama port-ka ay random ka dhigtaa
- **SMBv1**: Waxay damiyaa borotokoolka wadaagga faylasha ee duugan
- **ICMP**: Waxay ka hortagtaa jawaabaha ping-ga ee sirdoonka
- **LLMNR/NetBIOS**: Waxay xidhataa borotokooladka xallinta magacyada ee duugan

#### Amniga Codsiyada
- **Makrooska**: Waxay damiyaa fulinta makrooska codsiyada Office
- **AutoRun**: Waxay ka hortagtaa fulinta otomaatig ah warbaahinta la qaadi karo

#### Maamulka Fog
- **PSRemoting**: Waxay damiyaa kalfadihii PowerShell fog
- **WinRM**: Waxay joojisaa Windows Remote Management
- **Remote Assistance**: Waxay xidhataa xidhiidhka caawinta fog

#### Xakamaynta Gelitaanka
- **Admin Shares**: Waxay damiyaa wadaagga C$, ADMIN$
- **Guest Account**: Waxay damiyaa gelitaanka akoonka martida
- **USB Storage**: Waxay xaddidaysaa isticmaalka qalabka USB

### Isdhexgalka Azure
```powershell
# Ku xidhiidh Azure tenant
Connect-AzureGhost -Interactive

# Awood sii defaults-ka amniga
Set-AzureSecurityDefaults -Enable

# Qaabeey gelitaanka shuruudaysan
Set-AzureConditionalAccess -BlockLegacyAuth -RequireMFA

# Soo baadh isticmaalayaasha mudanayaasha ah
Set-AzurePrivilegedUsers -AuditOnly
```

### Isdhexgalka Intune (Cusub v2-ga)
```powershell
# Ku xidhiidh Intune
Connect-IntuneGhost -Interactive

# Geey iyada oo loo marayo siyaasadaha Intune
Set-IntuneGhost -Settings @{
    RDP = $true
    SMBv1 = $true
    USBStorage = $true
    Macros = $true
}
```

## ⚠️ Tixraacyo Muhiim ah

### Shuruudaha Tijaabinta
- **Deegaanka Shaybaareed**: Marka hore ku tijaabow dhammaan goobaha deegaan gooni ah
- **Geyn Marxalad-marxalad**: Si tartiib ah u geey si aad u ogaato dhibaatooyinka
- **Qorshaha Dib-u-celinta**: Hubi inaad dib u celin karto isbeddellada haddii loo baahdo
- **Dukumentiga**: Qor goobaha shaqeeya deegaankaaga

### Saameynta Dhici Karta
- **Waxsoosaarka Isticmaalaha**: Qaar ka mid ah goobahu waxay saameyn karaan socdaalka shaqada maalinlaha ah
- **Codsiyada Duugan**: Nidaamyada duugan waxay u baahan yihiin borotokoolal gaar ah
- **Gelitaanka Fog**: Ka feker saameynta maamulka fog ee xaqa ah
- **Nidaamyada Ganacsiga**: Xaqiiji inaan goobahu jabinin shaqooyinka muhiimka ah

### Xaddidaadka Amniga
- **Difaaca Gujinta**: Ghost waa hal lakab amni, ma aha xal buuxa
- **Maaraynta Joogtada ah**: Amnigu wuxuu u baahan yahay la socodka iyo cusboonaysiinta joogtada ah
- **Tababarka Isticmaalaha**: Xakamaynta farsamaysan waa inay la mid noqoto miyirka amniga
- **Horumarinta Khataraha**: Hababka weerar ee cusub waxay dhaafi karaan ilaalinta hadda jirta

## 🎯 Tusaalayaasha Xaalado Weerar

In kastoo Ghost uu bartilmaameedsado waddooyinka weerarka caadiga ah, ka-hortagga gaarka ah wuxuu ku xiran yahay fulinta iyo tijaabinta saxda ah:

### Weerarrada Qaabka WannaCry
- **Yaraynta**: `Set-Ghost -SMBv1` wuxuu damiyaa borotokoolka nugul
- **Tixraacyo**: Hubi inaan nidaam duug ah loo baahnin SMBv1

### Ransomware-ka ku Salaysan RDP
- **Yaraynta**: `Set-Ghost -RDP` wuxuu xidhaaa gelitaanka desktop fog
- **Tixraacyo**: Waxay u baahan tahay hababka kale ee gelitaanka fog

### Malware-ka ku Salaysan Dukumenti
- **Yaraynta**: `Set-Ghost -Macros` wuxuu damiyaa fulinta makrooska
- **Tixraacyo**: Waxay saameyn kartaa dukumentiyada xaqa ah ee makroo la hawl-geliyay

### Khataraha USB lagu Gudbiyay
- **Yaraynta**: `Set-Ghost -USBStorage -AutoRun` wuxuu xaddidayaa hawlgalka USB
- **Tixraacyo**: Waxay saameyn kartaa isticmaalka xaqa ah ee qalabka USB

## 🏢 Sifooyin Ganacsi

### Taageerada Group Policy
```powershell
# Ku dhaq goobaha iyada oo loo marayo diiwaanka Group Policy
Set-Ghost -SMBv1 -RDP -AutoRun -GroupPolicy

# Goobahu waxay ku shaqeeyaan domain oo dhan GP cusboonaysiinta ka dib
gpupdate /force
```

### Isdhexgalka Microsoft Intune
```powershell
# Samee siyaasadaha Intune ee goobaha Ghost
Set-IntuneGhost -Settings $GhostSettings -Interactive

# Siyaasadaha waxay si otomaatig ah ugu geeyaan qalabka la maareeyay
```

### Warbixinta Waafaqnimada
```powershell
# Dhal warbixin qiimaynta amniga
Get-Ghost | Export-Csv -Path "SecurityAudit-$(Get-Date -Format 'yyyy-MM-dd').csv"

# Warbixinta mowqifka amniga Azure
Get-AzureGhost | Out-File "AzureSecurityReport.txt"
```

## 📚 Dhaqamada Ugu Fiican

### Ka Hor Geynta
1. **Dukumentiga Xaalada Hadda**: Socodsii `Get-Ghost` ka hor isbeddellada
2. **Si Taxaddar ah u Tijaabow**: Xaqiiji deegaan aan soosaaro ahayn
3. **Qorshe Dib-u-celinta**: Ogow sida loo dib u celiyo goob kasta
4. **Dib-u-eegista Daneeyayaasha**: Hubi in qeybaha ganacsiga ay ansixiyaan isbeddellada

### Geynta Inta Lagu Jiro
1. **Habka Marxalad-marxalad**: Marka hore u geey kooxaha duuliyaha
2. **La-soco Saameynta**: Eeg cabaadka isticmaalayaasha ama dhibaatooyinka nidaamka
3. **Dukumentiga Dhibaatooyinka**: Qor dhibaato kasta oo tixraac mustaqbal ah
4. **Isdhaafsiga Isbeddellada**: U soo sheeg isticmaalayaasha hagaajinta amniga

### Geynta Ka Dib
1. **Qiimayn Joogto ah**: Si weyn u socodsii `Get-Ghost` si aad u xaqiijiso goobaha
2. **Cusboonaysii Dukumentiga**: Hay qaabeynta amniga hadda jirta
3. **Dib u eeg Waxtarka**: La-soco dhacdooyinka amniga
4. **Hagaajin Joogto ah**: Habeey goobaha iyaga oo ku saleysan muuqaalka khatarta

## 🔧 Xallinta Dhibaatada

### Dhibaatooyinka Caadiga ah
- **Khaladaadka Fasaxa**: Hubi kalf PowerShell la sarraysiiyay
- **Ku-tiirsanaanta Adeegga**: Qaar ka mid ah adeegyadau waxay yeelan karaan ku-tiirsan
- **Waafaqnimada Codsiga**: Ku tijaabow codsiyada ganacsiga
- **Xidhiidhka Shabakada**: Xaqiiji in gelitaanka fog uu weli shaqeynayo

### Ikhtiyaarrada Soo-celinta
```powershell
# Dib u hawl-geli adeegyo gaara haddii loo baahdo
Set-RDP -Enable
Set-SMBv1 -Enable
Set-AutoRun -Enable
Set-Macros -Enable
```

## 👨‍💻 Qoraha

**Jim Tyler** - Microsoft MVP PowerShell
- **YouTube**: [@PowerShellEngineer](https://youtube.com/@PowerShellEngineer) (10,000+ ruukun ah)
- **Warqadda**: [PowerShell.News](https://powershell.news) - Sirta amniga usbuuciga
- **Qoraha**: "PowerShell for Systems Engineers"
- **Khibrad**: Tobanaan sano ee PowerShell otomaatig iyo amniga Windows

## 📄 Shati iyo Diidumo

### Shatiga MIT
Ghost waxaa la bixiyaa shatiga MIT ee isticmaalka, wax ka beddelka iyo qaybinta bilaashka ah.

### Diidumo Amniga
- **Ma jiro Damaanad**: Ghost waxaa la bixiyaa "sida uu yahay" iyada oo aan lahayn damaanad nooc kasta ah
- **Tijaabin Loo baahan yahay**: Had iyo jeer marka hore ku tijaabow deegaannada aan soosaarka ahayn
- **Hagitaan Xirfadeed**: Kala tashi xirfadleyda amniga ee geynta wax soosaarka
- **Saameynta Hawlgelinta**: Qorayaashu mas'uul kama aha wax carqaladeyn hawlgal ah
- **Amni Dhamaystiran**: Ghost waa hal curiye istiraatiijiyada amniga buuxda

### Taageero
- **GitHub Issues**: [Soo sheeg khaladaad ama codsado sifooyinka](https://github.com/jimrtyler/Ghost/issues)
- **Dukumentiga**: Isticmaal `Get-Help <function> -Full` caawin faahfaahan
- **Bulshada**: PowerShell iyo bulshada amniga foormamka

---

**🔒 Xooji mowqifkaaga amniga Ghost - laakiin had iyo jeer marka hore tijaabow.**

```powershell
# Ku bilow qiimaynta, ma aha mala-awaalka
Get-Ghost
```

**⭐ Xiddigis kaydkan haddii Ghost uu kaa caawinayo in aad hagaajiso mowqifkaaga amniga!**