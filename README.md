gg.setVisible(false)
local tang = gg.alert("สคริปต์จัดเรียงโดย: อ้าย'ย ตัง'ง ชาแนล\nถ้ากลัวติดดำก็ออกไปไอควาย","เข้าใช้งาน","ทางออก")
if tang == 1 then gg.toast("สถานะ: ✅ออนไลน์✅",true) else end
if tang == 2 then os.exit(0) end

local n, startAddress, endAddress = nil, 0, 0
local function name(lib)
	if n == lib then
		     return startAddress, endAddress end
	local ranges = gg.getRangesList(lib or 'libanogs.so') -- ตัวคำนวณลิป
	for i, v in ipairs(ranges) do
		if v.state == "Xa" then
			startAddress = v.start
			endAddress = ranges[#ranges]['end']
			break
		end
	end
	return startAddress, endAddress
end
local function AsdMemory(libname, offset, hex)
	name(libname)
	local t, total = {}, 0
	for h in string.gmatch(hex, "%S%S") do
	    table.insert(t, {
	        address = startAddress + offset + total,
	        flags = gg.TYPE_BYTE,
	        value = h .. "r"
	    })
	    total = total + 1
	end
	local res = gg.setValues(t)
	if type(res) ~= 'string' then
		return true
	else
		gg.alert(res)
		return false
	end
end


AsdMemory("libanogs.so",0x39AD5C4,"00 00 00 00")
AsdMemory("libanogs.so",0x181B8A0,"00 00 00 00")


gg.setVisible(true)
function main()
menu=gg.choice({
"Rᴇɢᴡᴅɪᴛ 8.0", --1
"Aɪᴍʟᴏᴄᴋ Pʀᴏ", --2
"Cʟᴇᴀʀ Mᴀᴘs", -- 3
"Cᴀᴍᴇʀᴀ Hɪɢʜᴛ",
"Aɴᴛᴇɴᴀ Yᴇʟʟᴏᴡ",
"แสดงเลือกตอนยิง",
"Rᴇᴍᴏᴠᴇ Dᴇʟᴇᴀs",
"Eғғᴇᴄᴛ Sʜᴏᴛ Gᴜɴs",
"ปิดเอฟเฟ็กตอนยิง",
"ดูดหัวทุกปืนล่าสุด",
"Exɪᴛᴇᴅ Sᴄʀɪᴘᴛ"},0,os.date("Mod hack by : Ar Jarn Tang Rachapro\nclock -> %r\ndates -> %A/%B/%Y"))
if menu == nil then os.exit(0) else
if menu == 1 then a1() end
if menu == 2 then a2() end
if menu == 3 then a3() end
if menu == 4 then a4() end
if menu == 5 then a5() end
if menu == 6 then a6() end
if menu == 7 then a7() end
if menu == 8 then a8() end
if menu == 9 then a9() end
if menu == 10 then a10() end
if menu == 11 then a11() end
end
asd=-1
end
function a1()
gg.clearResults(16384)
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber(";bone_Spine",gg.POINTER_EXECUTABLE_WRITABLE,false,gg.SIGN_EQUAL,0,-1,0)
var = gg.getResults(16384)
gg.editAll(";bone_Head1",gg.POINTER_EXECUTABLE)
gg.clearResults(16384)
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber(";Bip01",gg.POINTER_EXECUTABLE)
var = gg.getResults(2000)
gg.editAll(";Bip00",gg.POINTER_EXECUTABLE)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("-0.0446202829",gg.POINTER_WRITABLE,false,gg.SIGN_EQUAL,0,-1)
var = gg.getResults(300)
gg.editAll("0.0,2",gg.POINTER_WRITABLE)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("-0.0388151556",gg.POINTER_WRITABLE,false,gg.SIGN_EQUAL,0,-1)
var = gg.getResults(300)
gg.editAll("0.0,4",gg.POINTER_WRITABLE)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber(";Bip01",gg.POINTER_EXECUTABLE)
var = gg.getResults(999)
gg.editAll(";Bip00",gg.POINTER_EXECUTABLE)
gg.clearResults()
gg.searchNumber("0.07869631797;0.99689865112;1.0;1.0;1.0::17",gg.POINTER_WRITABLE)
gg.refineNumber("1", 16)
var = gg.getResults(999)
gg.editAll("1.5",gg.POINTER_WRITABLE)
gg.clearResults()
gg.searchNumber("0.98958933353;1.0;1.0;1.0::17",gg.POINTER_WRITABLE)
gg.refineNumber("1", 16)
var = gg.getResults(99)
gg.editAll("1.5",gg.POINTER_WRITABLE)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a2()
  gg.setRanges(gg.REGION_ANONYMOUS)
  gg.searchNumber("0.84705883265;0.5;0.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
  gg.processResume()
  gg.refineNumber("0.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
  revert = gg.getResults(52000, nil, nil, nil, nil, nil, nil, nil, nil)
  gg.editAll("10", gg.TYPE_FLOAT)
  gg.processResume()
  gg.setRanges(gg.REGION_C_HEAP | gg.REGION_C_ALLOC)
  gg.searchNumber("40800000h", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
  gg.getResults(400)
  gg.clearResults()
  gg.setRanges(gg.REGION_VIDEO)
  gg.searchNumber("0.23000000417", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
  gg.getResults(100)
  gg.editAll("-50", gg.TYPE_FLOAT)
  gg.clearResults()
  gg.setRanges(gg.REGION_ANONYMOUS)
  gg.searchNumber("00002042rD;00004040rD;00007042rD;A470FD3ErD;AE47013FrD;A470FD3ErD;AE47013FrD;AE47E13ErD;295C0F3FrD;14AEC73ErD;F6281C3FrD;0000C03FrD:49", 13, false, 536870912, 0, -1)
  gg.getResults(1000)
  gg.editAll("-20000;-20000;-20000;-20000;-20000;-20000;-20000;-20000;-20000;-20000;-20000;1,148,829,696", 4)
  gg.clearResults()
  gg.setRanges(gg.REGION_CODE_APP | gg.REGION_CODE_SYS)
  gg.searchNumber("-1.30928164e25;-3.69511377e20;1.25206298e-38;0.00001", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
  gg.refineNumber("0.00001", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
  revert = gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)
  gg.editAll("1", gg.TYPE_FLOAT)
  gg.clearResults()
  gg.processResume()
  gg.setRanges(gg.REGION_ANONYMOUS)
  gg.searchNumber("1.35000002384", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
  gg.getResults(1000)
  gg.editAll("100", gg.TYPE_FLOAT)
  gg.clearResults()
  gg.toast("ঔৣ‌➳Script Done")
end
function a3()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("0.15", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1000)
gg.editAll("1000", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a4()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("3.14159274101",gg.POINTER_WRITABLE,false,gg.SIGN_EQUAL,0,-1)
var = gg.getResults(1000)
gg.editAll("5",gg.POINTER_WRITABLE)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a5()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber(";ingame/capsulehumansnipercollider",gg.POINTER_EXECUTABLE)
var = gg.getResults(2000)
gg.editAll(";effects/ff_fx_guide_arrow",gg.POINTER_EXECUTABLE)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a6()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("0.1",gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(1000,nil,nil,nil)
gg.editAll("0.100",gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a7()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("0.2",gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(1000,nil,nil,nil)
gg.editAll("0",gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a8()
b=gg.prompt({"ปรับความเข้มของเอฟเฟก[1;150]"},b,{"number"})
if b == nil then os.exit() end
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("0.3",gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(1000,nil,nil,nil,nil)
gg.editAll(''..b[1]..'',gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a9()
b=gg.prompt({"ปรับตามจำนวนที่เปิด[1;150]"},b,{"number"})
if b == nil then os.exit() end
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber(''..b[1]..'',gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(1000,nil,nil,nil,nil)
gg.editAll("0.3",gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a10()
b=gg.prompt({"ความเเม่นของดูดหัวแนะนำปรับ -3[-4;4]"},b,{"number"})
if b == nil then os.exit() end
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("40.0",gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(1000,nil,nil,nil,nil)
gg.editAll(''..b[1]..'',gg.TYPE_FLOAT)
gg.clearResults()
b=gg.prompt({"ความไวของหน้าจอหรือdpi เเนะนำปรับ 240[0;280]"},b,{"number"})
if b == nil then os.exit() end
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("300",gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(1000,nil,nil,nil,nil)
gg.editAll(''..b[1]..'',gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("ঔৣ‌➳Script Done")
end
function a11()
print("Tʜᴀɴᴋ ғᴏʀ ᴜsᴇ ᴍʏ sᴄʀɪᴘᴛ : Gᴏᴏᴅ Lᴜᴄᴋ ❤")
print(os.date("Dᴇᴛᴇ&Tɪᴍᴇ➤ : %x • %X"))
os.exit()
end
while true do
if gg.isVisible(true) then
asd = 1
gg.setVisible(false) end
if asd == 1 then
main() end end
