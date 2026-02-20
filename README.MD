### **Serveurs DM CS2**
- [Pracc](https://pracc.com/play)
- [Cybershoke](https://cybershoke.net/cs2)
- [Warmup Server](https://www.warmupserver.net/servers_filters.php)

## **Optimisation des Performances – CS2 / Windows 11**

### **Options de Lancement CS2**
Utilisez ces paramètres pour optimiser le lancement du jeu :
```bash
-threads 16 -tank_WorkerThreadCount 16 +exec autoexec.cfg
```

---

## **Optimisation Windows 11**

### **1. Alimentation**
- **Plan d’alimentation** : *Performances élevées*

### **3. Mises à jour**
- **Désactiver** : Mises à jour automatiques des pilotes

### **4. Désactiver les Services Inutiles**

#### **Xbox Game Bar**
Exécutez ces commandes PowerShell :
```powershell
Get-AppxPackage *XboxGamingOverlay* | Remove-AppxPackage
Get-AppxPackage *XboxIdentityProvider* | Remove-AppxPackage
Get-AppxPackage *Xbox* | Remove-AppxPackage
```

#### **Game DVR (via Registre)**
```powershell
Set-ItemProperty -Path "HKCU:\System\GameConfigStore" -Name "GameDVR_Enabled" -Value 0 -Type DWord
```

#### **Services Liés (Optionnel)**
```powershell
Stop-Service -Name "XboxGipSvc" -Force
Set-Service -Name "XboxGipSvc" -StartupType Disabled
```

#### **Game Bar (via Paramètres Windows)**
```powershell
Set-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\GameDVR" -Name "AppCaptureEnabled" -Value 0 -Type DWord
```

---

## **Options du Jeu – CS2**

### **Emplacement des Fichiers**
- **Autoexec** : `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg`
- **Autres fichiers** : `C:\Program Files (x86)\Steam\userdata\*\730\local\cfg`

### Audio Settings
- **Master Volume** 100
- **Main Menu Ambience Volume** 0
- **Audio Device:** DEFAULT DEVICE
- **EQ Profile:** CRISP
- **L/R Isolation:** 50%
- **Perspective Correction:** NO
- **Play Audio When Game in Background:** YES

### **Paramètres d’Affichage**
- **Brightness** : 100

| Paramètre | Valeur |
|-----------|--------|
| Boost Player Contrast | **Activé** |
| V-Sync | **Désactivé** |
| NVIDIA G-Sync | **Désactivé** |
| NVIDIA Reflex Low Latency | **Activé + BOOST** |
| Maximum FPS In Game | 0
| Maximum FPS In Menus | 0
| Multisampling Anti-Aliasing Mode | **4X MSAA**
| Global Shadow Quality | **LOW**
| Dynamic Shadows | **ALL**
| Model / Texture Detail | **HIGH**
| Texture Filtering Mode | **ANISOTROPIC 2X**
| Shader Detail | **LOW**
| Particle Detail | **LOW**
| Ambient Occlusion | **Désactivé**
| High Dynamic Range | **PERFORMANCE**
| FidelityFX Super Resolution | **Désactivé (HIGHEST QUALITY)**

---
