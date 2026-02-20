<p align="center">
  <img src="https://raw.githubusercontent.com/tylergehm/printers/main/printeroffline.jpg" alt="GitHub banner" style="max-width:100%;height:auto;" />
</p>

# 🖨️ Printers: Common Issues & Fixes

> **🗣️ Printer Mantra**  
> _"If it’s not the **spooler**, it’s the **driver**. If it’s not the driver — **unplug it**."_

---

## 📋 Common Issues at a Glance

| # | **Issue**                                  | **Fix**                          |
|---|--------------------------------------------|----------------------------------|
| 1 | Printer Shows **"Offline"**                | Restart Print Spooler            |
| 2 | Print Jobs **Stuck in Queue**              | Clear Print Queue                |
| 3 | **"Driver is unavailable"** / Not Printing | Reinstall Driver                 |
| 4 | **Paper Jam** or "Jam in Tray" Error       | Power Cycle + Check Trays        |
| 5 | **Printing Blank Pages**                   | Check Ink/Toner + Clean Heads    |

---

## 🔧 Detailed Fixes

---

### 1. 🖥️➡️⚫ Printer Offline
**Symptoms**  
- Shows **"Offline"** in **Devices and Printers**  
- Jobs queue but **never print**  
- Can ping IP → still not working

**Root Causes**  
- Print Spooler **crashed**  
- Corrupted job in queue  
- Network hiccup / SNMP mismatch

**Fix Steps**  
1. `Win + R` → `services.msc` → **Enter**  
2. **Print Spooler** → Right-click → **Restart**  
3. Wait 10 sec  
4. Power cycle **printer**  
5. Set as **default**

**Result:** Status → **"Ready"**

---

### 2. 📄⏳ Jobs Stuck in Queue
**Symptoms**  
- Old jobs **won’t cancel**  
- New jobs show **“Error - Printing”**  
- Queue shows **10+ stuck docs**

**Root Causes**  
- Corrupted PDF/large file  
- Printer went offline mid-job  
- Spooler locked by process

**Fix Steps**  
1. Open **Devices and Printers**  
2. Right-click printer → **See what’s printing**  
3. **Printer menu** → **Cancel All Documents**  
4. If stuck → Restart **Print Spooler** (Fix #1) or reboot PC

**Tip:** Stuck jobs is a common cause of printers being "offline"

---

### 3. 🚫💾 Driver Unavailable / Corrupted
**Symptoms**  
- **"Driver is unavailable"** error  
- Generic driver (no duplex/color)  
- Test page fails

**Root Causes**  
- Windows Update overwrote driver  
- Corrupted install package  
- Missing printer software

**Fix Steps**  
1. Right-click printer → **Remove device**  
2. `Win + X` → **Device Manager**  
3. **Print queues** → Uninstall device  
4. **Action** → **Scan for hardware changes**  
5. Or download from **HP | Brother | Canon**

**Auto-fix:** Windows 10/11 usually reinstalls

---

### 4. 📄🚧 Paper Jam
**Symptoms**  
- **"Jam in Tray 1"** or flashing light  
- Paper stuck halfway  
- No jam but error persists

**Root Causes**  
- Paper fragment in rollers  
- Dust on sensors  
- Worn pickup rollers  
- False trigger (heat/humidity)

**Fix Steps**  
1. **Unplug printer** (30 sec)  
2. Open **all trays & doors**  
3. Remove paper — **pull forward only**  
4. Check **rear access panel**  
5. Plug in → print **test page**

**Pro Tip:** Clean rollers monthly to prevent

---

### 5. ⚪📄 Printing Blank Pages
**Symptoms**  
- Pages **completely white**  
- Ink/toner shows **full**  
- Test page also blank

**Root Causes**  
- Clogged print heads (dried ink)  
- Fake cartridge  
- Toner not fusing  
- Misaligned head contact

**Fix Steps**  
1. Print **nozzle check** / **test pattern**  
2. Run **cleaning cycle** (1–2x)  
3. Re-seat **ink/toner**  
4. Replace if dried  
5. Laser: Gently shake toner

**Mac Users**  
> 🍎 System Settings → Printers & Scanners → Right-click list → **Reset printing system**
