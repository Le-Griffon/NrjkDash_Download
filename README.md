# NrjkDash
Download Windows and Android versions from Releases.

Choosing an ELM327 dongle for your Energica (NrjkDash) 🏍️⚡

Not all ELM327 dongles are equal. Here’s what actually matters:

✅ Genuine ELM327 v1.4b+ or an STN chip (OBDLink). Cheap “v2.1” clones are often v1.0 copies with a fake version number.
✅ ATCEA support (CAN extended addressing). Energica diagnostics need it, and many clones answer “?”.
✅ Solid ATMA + hardware filters (ATCRA / ATCF / ATCM). The bike’s CAN bus runs about 1,300 frames/s at 500 kbit/s, and weak dongles overflow (“BUFFER FULL”) and drop frames.
✅ BLE or Bluetooth Classic. BLE is needed for iPhone; Classic usually gives more throughput (Android/Windows).

❌ Avoid no-name “v2.1/v2.2” dongles and anything that doesn’t answer ATI / AT@1 properly.

🔧 Quick test before you trust one:

ATI → check the version
ATCEA F1 → must reply OK
ATCRA 200 then ATMA, ignition on → steady 0x200 frames, no “BUFFER FULL”

👍 I use Veepeak OBDCheck BLE+.
👍 Known solid options: OBDLink CX (BLE) or OBDLink MX+ (Classic). They meet the specs on paper; I haven’t tested them on an Energica yet.
