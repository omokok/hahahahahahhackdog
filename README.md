gg.alert('SCRIPT RUNS IN 10SECS','')
gg.sleep(10000)
gg.sleep(300)
gg.toast("▓▒▒▒▒▒▒▒▒▒10%")
gg.sleep(300)
gg.toast("▓▓▒▒▒▒▒▒▒▒20%")
gg.sleep(300)
gg.toast("▓▓▓▒▒▒▒▒▒▒30%")
gg.sleep(300)
gg.toast("▓▓▓▓▒▒▒▒▒▒40%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▒▒▒▒▒50%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▒▒▒▒60%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▓▒▒▒70%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▓▓▒▒80%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▓▓▓▒90%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▓▓▓▓100%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▓▓▓▒90%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▓▓▒▒80%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▓▒▒▒70%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▓▒▒▒▒60%")
gg.sleep(300)
gg.toast("▓▓▓▓▓▒▒▒▒▒50%")
gg.sleep(300)
gg.toast("▓▓▓▓▒▒▒▒▒▒40%")
gg.sleep(300)
gg.toast("▓▓▓▒▒▒▒▒▒▒30%")
gg.sleep(300)
gg.toast("▓▓▒▒▒▒▒▒▒▒20%")
gg.sleep(300)
gg.toast("▓▒▒▒▒▒▒▒▒▒10%")
gg.sleep(300)
gg.toast("▒▒▒▒▒▒▒▒▒▒0%")
gg.sleep(300)
gg.setVisible(false)
hehe = gg.alert(os.date([[
═क════ ⊹⊱✫⊰⊹ ════क═
Fiture Encrypt🛡 :
➣ New Blocker & Base
➣ Hide String + Random + Hard Key
➣ Big Lasm & Big Log. 
➣ Crash SsTool + Bypass 1-0.
➣ Auto Make Blocker SSTools + TC (BETA)
➣ Filter ++  : 
 • Set Expired Date
 • Set Password Script
 • Set Minim GG
 • Set Package GG
 • Set Auto Detected GG Decrypt
 • Set Lua Header
 
═क════ ⊹⊱✫⊰⊹ ════क═
@ASHLEYRAMIREZ
]]),'🛡️ Encrypt', '🔍 About', '❎Exit')
if hehe == 1 then
local g = {};local FD = {}
g.last = gg.getFile()
g.info = nil
g.config = gg.EXT_CACHE_DIR .. "/" .. gg.getFile():match("[^/]+$") .. "cfg"
g.data = loadfile(g.config)
if g.data ~= nil then g.info = g.data() g.data = nil end
if g.info == nil then g.info = {g.last, g.last:gsub("/[^/]+$", "")} end
while true do
g.info = gg.prompt({
"📁 Choose Script to ASHLEY ENCRYPT: ",--1
"📁 Select Output Folder: ",--2
"🕒 Add Expirity Date",--3
"🔐 Add Password",--4
"🛡️ Add Minimal GG Required",--5
"🗳 Add Package GG",--6
"⚠️ Add Auto Detected AshleyDecrypt",--7
},g.info,{
"file",--1
"path",--2
"checkbox",--3
"checkbox",--4
"checkbox",--5
"checkbox",--6
"checkbox",--7
})
if g.info == nil then break end
gg.saveVariable(g.info,g.config)
DATA = io.input(g.info[1]):read("*a")
if not load(DATA) then os.exit() end

if g.info[3] == true then
day = os.date("%d")
exp_date = gg.prompt({
"📆 Set Expired Date : ",
"📝 Type Expired Message : "},
{os.date("%Y%m" .. day + 7),"🇵🇱ASHLEYEXPIRED🇵🇱"},{"number", "text"})
end
if not exp_date then
gg.setVisible(true)
elseif exp_date[1] == nil then gg.alert("📆 Date Can Not Be Empty !") gg.setVisible(true)
else
print("\n📅 Added Expired Date : ".. exp_date[1])
DATA = '\n if os.date("%Y%m%d") >= "' ..exp_date[1].. '" then print("'..exp_date[2]..'") return gg.alert("' ..exp_date[2] ..'")end\n' .. DATA
end

if g.info[4] == true then
PASS = gg["prompt"]({
"🔐 Set Password For Script :",
"📝 Type Message For Wrong Password : "
}, {"","🇵🇱WRONG PASSWORD ASHLEY🇵🇱"},{
"text",
"text"})
end
if not PASS then
gg.setVisible(true)
elseif PASS[1] == nil then
gg.alert("⚠️ Input Password !")
gg.setVisible(true)
else
print("\n🔐Added Password Script : ".. PASS[1])
DATA = 'PASSW = gg.prompt({\'🔒 Input password: \'},{[1]=\'\'},{[1]=\'text\'})\nif not PASSW the﻿n return\nend \nif PASSW[1] == "" then gg.alert("Password Can Not Be Empty❕") end\nif PASSW[1] =="' .. PASS[1] .. '" then\ngg.toast(\'✅ Password correct❕\')\nelse\nreturn gg.alert("' .. PASS[2] .. '") end\n' .. DATA
end

if g.info[5] == true then
VERSION = gg.prompt({
"🔐 Set Minimal GG Version : ",
"🗒️ Set Error GG Message :"
}, {gg.VERSION,"🇵🇱ERROR GG ASHLEY🇵🇱"}, {
"number",
"text"})
end
if not VERSION then
gg.setVisible(true)
elseif VERSION[1] == nil then
gg.alert("🛡️ Input Minimal Required GG Version !")
gg.setVisible(true)
else
print("\n🛡️Added Minimal GG Version : "..VERSION[1])
DATA = '\n if gg.VERSION < "'..VERSION[1] .. '" then print("'..VERSION[2]..'") return gg.alert("' ..VERSION[2].. '")end\n' .. DATA
end

if g.info[8] == true then
ASHLEYRAMIREZPROENC = gg.prompt({
"✏️ Set Your Package GameGuardian",
"📝 Type Message If Package Is Wrong :"
}, {"com.GameGuardian.id","⚠ Use MY GG For Run This Script ⚠"},{
"text",
"text"})
end--if
if not ASHLEYRAMIREZPROENC then
gg.setVisible(true)
elseif ASHLEYRAMIREZPROENC[1] == nil then
gg.alert("⚠️ Set Package GameGuardian Can Not Bd Empty!")
gg.setVisible(true)
else
print("⚠ SetPeckage GG : True√ ")
DATA = '\nif gg.PACKAGE == "' .. ASHLEYRAMIREZPROENC[1] .. '" then\nelse\ngg.alert("' .. ASHLEYRAMIREZPROENC[2] .. '")\nprint("' .. ASHLEYRAMIREZPROENC[2] .. '")\nos.exit()\nend\n' .. DATA
end

if g.info[8] == true then
DATA = ([[if gg.isPackageInstalled("com.minhui.networkcapture") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("com.goushi.gtpcanary") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("com.packagesniffer.frtparlak") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("com.rhmsoft.edit") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("app.greyshirts.sslcapture") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("frtparlak.rootsniffer") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("com.minhui.wifianalyzer") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("jp.co.taosoftware.android.packetcapture") then
  print("Desinstale o Packet Capture")
  os.exit()
else
end
if gg.isPackageInstalled("com.prabalMSWKPRO.logger") then
  print("uninstall your logger gg to Run Script")
  os.exit()
else
end
if gg.isPackageInstalled("any_.body_.can_.fuck_.tencent_") then
  print("uninstall ur DeAshleyRamirezOfficialpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.s.fyojrme") then
  print("uninstall ur DeAshleyRamirezOfficialpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.rjvsbmhdspmnfbame") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.redwolfMSWKPRO.ripgg") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.vrexqfftfsxekm.kl") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.nochqxpucsbldqqx") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.ghueczxrttlhgd") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.yy.qptvrjwerw.ghoex") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.nochqxpucsbldqqx") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.pvt4u") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.Egypt.yuosseef") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.tssfjipkmrco") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.vip.paidhacksonly.mr.toxin") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.ioyysvgfsrig") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.mrteamz.id") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.jtbodgpqxox") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.eidymumcghpfeeeavps") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.mod.iraq") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.dzelttwyuyyes") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.sxqa") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.xyyxgxfn") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.zgb") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.tssfjipkmrco") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.vnpqk") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.mwjvnwesbghkxbjznbwo") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.blackduty.gc") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.s.fyojrme") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.roxmemek") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.fhshwhpvqvruvjtu") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.fireonMSWKPRO.fog") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.paranoiaworks.unicus.android.sse") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.raincityMSWKPRO.ggmod") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.pvt4u") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.nydpvsb.z.r.pkgh") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.ioyysvgfsrig") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.gmsm") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.sudsjcqvvcmgutdjeg") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.redwolfMSWKPRO.ripgg") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.coolfoolggfuckscript.tm") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.eidymumcghpfeeeavps") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.dzelttwyuyyes") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.foxcyber.gg") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.sxqa") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("com.zgb") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("catch_.me_.if_.you_.can_") then
  print("uninstall ur DeAshleyRamirezpt GG")
  os.exit()
end
if gg.isPackageInstalled("sstool.only.com.sstool") then
  print("Uninstall SSTOOL Deceypt")
  os.exit()
end
if gg.isPackageInstalled("sstool.only.com.sstool") then
  print("Uninstall SSTOOL Deceypt")
  os.exit()
end
if gg.isPackageInstalled("catch_.me_.if_.you_.can_") then
  print("Uninstall orginal GG")
  os.exit()
end
]])..DATA
print('🛡 Auto Detect DeAshleyRamirezpt : True √ ')
end

g.last = g.info[1]
g.out = g.last:match("[^/]+$")
g.out = g.out:gsub(".lua", ".𝙰𝚂𝙷𝙻𝙴𝚈")
g.out = g.info[2]..'/'..g.out..'.𝙰𝚂𝙷𝙻𝙴𝚈'
local DATA = io.input(g.last):read('*a')


AB = math.random(1000,20000)
AC = math.random(3000,40000)
AD = math.random(5000,60000)
AE = math.random(7000,80000)
AF = math.random(9000,100000)
AG = math.random(300,600)
local key = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF}
local KY1 = (key[5]+key[2]+key[1]*key[4])-key[1] local KY2 = (key[2]+key[3]*1)-key[4]
function enc(str)
str = str:gsub("\\n", "\n"):gsub("\\t","\t")
gb = {str:byte(0,-1)}
res = ''
LASM = '\\014'
for i = 1, #gb do
gb[i] = (gb[i] - KY1 - (KY2 + i) * (KY1 + i) ) % 256
end
return "{"..table.concat(gb, ",").."}"
end

local encode = function(c)
return 'string.char(table.unpack({'..LEGS(c)..'}))'
end
local AllKeys = ([[
local HideKey1 = math.random(10000,100000)
local wonggendeng = math.random(10000,100000)
local HideKey2 = math.random(10000,100000)
local yokoenikusengedan = math.random(10000,100000)
local HideKey3 = math.random(10000,100000)
local LUA = math.random(10000,100000)
local Lol = math.random(10000,100000)
local Asu = math.random(10000,100000)
local AH = math.random(10000,100000)
local AG = math.random(10000,100000)
local AF =math.random(10000,100000)
local AE = math.random(10000,100000)
local AD = math.random(10000,100000)
local AI = math.random(10000,100000)
local AB = math.random(10000,100000)
local AC = math.random(10000,100000)
local AA = math.random(10000,100000)
local edaaan = math.random(10000,100000)
local wongAshleyRamirez = math.random(10000,100000)
local ccccccrrr = math.random(10000,100000)
]])

local encode = function(c)
return table.concat({c:byte(1,-1)}, ",")
end
local EnAshleyRamirezptKeys = AllKeys:gsub('%"(.-)%"', function(c)
c = load('return "'..c..'"')()
c = encode(c)
return 'string.char(table.unpack({'..c..'}))'
end)

local DATA = ([[
]]..EnAshleyRamirezptKeys..[[
local wongedankuwibebas = function(str) 
local KeyHard, KeyAshleyRamirezy = HideKey2, AI + HideKey3
return (str:gsub("%x%x", function(KeyAshleyRamirezyy) 
KeyHard = KeyHard % AA
KeyAshleyRamirez = (KeyHard - KeyHard) / AA
KeyAshleyRamirezy = KeyAshleyRamirez % wongAshleyRamirez
KeyAshleyRamirezyy = tonumber(KeyAshleyRamirezyy, edaaan) 
KeyAshleyRamirez = (KeyAshleyRamirezyy + (KeyAshleyRamirez - KeyAshleyRamirezy) / wongAshleyRamirez) * (2*KeyAshleyRamirezy + 1) % ccccccrrr
KeyHard = KeyHard * KeyAshleyRamirezy + KeyAshleyRamirez + KeyAshleyRamirezyy + KeyAshleyRamirez 
return string.char(KeyAshleyRamirez)end))
end
]]..DATA)

DATA =[[
local function _8()
]]..DATA..[[

end
_8()
]]

function encodegg(A0_67)
	return 'gg[SHA({AshleyRamirezOfficial = "' .. Sha(A0_67) .. '"})]('
end
function encodeggg(A0_67)
	return '' .. enc(A0_67) .. ')'
end
function encodeos(A0_68)
	return 'os[AshleyRamirezOfficial(\n' .. enc(A0_68) .. '\n)]('
end
function encodeos(A0_68)
	return 'io[AshleyRamirezOfficial(\n' .. enc(A0_68) .. '\n)]('
end
function encodestr(A0_69)
	return 'string[AshleyRamirezOfficial(\n' .. enc(A0_69) .. '\n)]('
end
function encvalues(A0_70)
	return 'AshleyRamirezOfficial(\n' .. enc(A0_70) .. '\n)'
end

AshleyRamirez =[[
local AB = "]]..AB..[[";local iimi = "171";local AC = "]]..AC..[[";local iimi = "4817";local AD = "]]..AD..[[";local AE = "]]..AE..[[";local iimi = "371";local AF = "]]..AF..[[";local AG = "]]..AG..[[";local iimi = "13716";local key = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF};local KY1 = (key[5]+key[2]+key[1]*key[4])-key[1];local KY2 = (key[2]+key[3]*1)-key[4]
function AshleyRamirez(c)
res = ""
for m in ipairs(c) do
res = res..string.char((c[m] + KY1 + (KY2 + m) * (KY1 + m)) % 256)
end
return res
end
local Key53 = 8186484168865098;local Key14 = 4887;local inv256
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
local SHA = function(data)
data = data.AshleyRamirez
local K, F = Key53, 16384 + Key14 return (data:gsub('%x%x', function(c) local L = K % 274877906944 local H = (K - L) / 274877906944 local M = H % 128 c = tonumber(c, 16) local m = (c + (H - M) / 128) * (2*M + 1) % 256 K = L * F + H + c + m return string.char(m)end))end
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
MFA4 = "address";MFA5 = "flags";MFA6 = "values";MFA7 = "ERROR\nRESTART SCRIPT";MFA8 = "";MFA9 = "";local gg = gg;local os = os;local io = io;local debug = debug;local math = math;local table = table;for i = 1,5 do;loadfile = loadfile;load = load;loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end;a = {};for i = 1, string.char(53,48,48,48,48) do;table.insert(a, {[MFA4] = 0 + i,[MFA5] = 4,[MFA6] = 0});end;t1 = os.time();for i = 1, 6 do;gg.removeResults(a);end;gg.clearList();t2, a = os.time(), MFA7;if t2 < t1 then;gg.alert(MFA8, "");do return end;return;end;if t2 > t1 then;a = MFA9;end;if os.difftime(t2, t1) > 2 then;return F(a, "");end;
for i = 1, 0 do;local ssss = {}if ssss ~= nil then;ssss.ssss=ssss.ssss()end;ssss=nil;end
for i = 1, 0 do;local ssss = {}if ssss ~= nil then;ssss.ssss=ssss.ssss()end;ssss=nil;end
for i = 1, 0 do;local AshleyRamirez = {}if AshleyRamirez ~= nil then;AshleyRamirez.AshleyRamirez=AshleyRamirez.AshleyRamirez(x)end;AshleyRamirez=nil;end
for i = 1, 0 do;local AshleyRamirez = {}if AshleyRamirez ~= nil then;AshleyRamirez.AshleyRamirez=AshleyRamirez.AshleyRamirez(x)end;AshleyRamirez=nil;end
for i = 1, 0 do;local AshleyRamirez = {}if AshleyRamirez ~= nil then;AshleyRamirez.AshleyRamirez=AshleyRamirez.AshleyRamirez(x)end;AshleyRamirez=nil;end
for i = 1, 0 do;local AshleyRamirez = {}if AshleyRamirez ~= nil then;AshleyRamirez.AshleyRamirez=AshleyRamirez.AshleyRamirez(x)end;AshleyRamirez=nil;end
for i = 1, 0 do local XxX = ({(-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil),(-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil),{nil},{nil},{nil},{nil},{},{},{},{},{},{},(-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil % nil*nil/nil),(-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil % nil*nil/nil),{} }) local GVV = {} local pc = (-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil % nil*nil/nil)pc() local xnXx = (-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil % nil*nil/nil) local TF = (-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil) local NHH ={} local NG ={} local HG =  {} local AGG = NG.HG.NHH.NG.HG.NHH.NG.HG(NHH.NG.HG({NHH.NG.HG}))()   NHH.NG.HG(NHH.NG.HG({NHH.NG.HG}))() local GHG = NHH.NG.NG.HG() ANNN():HG() NHH.NHH[X] =NHH[P]  local TC = {} local TFTC = TC(TF) local TFTV = TFTC({TFTC}) local TFTF=TFTC.NG TFTF() local BV = (-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil)   GHG:pc() TF(xnXx)({FHG})({pc}) TFTF(BV) TFTF(BV+2); if TFTF(BV) <= TFTF(BV+1) then pc(xnXx); TFTF(BV+3)({TFTF(BV)}) TFTF(TFTF(XxX()))() GHG(TFTF(XxX()))() GHG(TFTF(XxX()))() TFTF(TFTF(XxX()))() TFTF(TFTF(XxX()))() TFTV(TFTF(XxX()))() TFTV(TFTF(XxX()))() GHG(AGG())() GHG(AGG())() GHG(AGG())() HG({TFTF})();end;end
for i = 1, 0 do local AshleyRamirez = {} AshleyRamirez.sel = AshleyRamirez.data() if AshleyRamirez.data ~= nil then AshleyRamirez.sel = AshleyRamirez.data() end AshleyRamirez = nil end
for x =0,1,0 do if nil ~= nil then (-nil)((-nil)[nil] | nil | nil) local _ = {} _ = _() _ = -nil  _  = _():_(-nil)(-nil * 1)..-nil _ = _(-nil)(_) if _~= nil then   _ = _ (-nil * nil)()  _ = nil end  if _  == nil then  _ = {_, _(-nil)(-nil)(nil * 1, 1  << nil), -nil} end end local x = {} x[''] = x local t = (x)(x, x) t[1] = 1 end

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
while(nil)do;local y={}if(y.y)then;y.y=(y.y(y))end;end
while(nil)do;for y=y,y do;local y={}if(y.y)then;y.y=y.y(y)end;for yy=y.y,y.y,y.y do;local yy={}if(yy.y)then;yy.y=yy.y()end;for yyy=y,yy.y,y do;local yyy={}if(yyy.y)then;yyy.y=yyy.y(y)end;for yyyy=y,yy,yyy.y do;local yyyy={}if(yyyy.y)then;yyyy.y=yyyy.y(y)end;local yyyy={}if(yyyy.y)then;yyyy.y=(yyyy|yyy|yy|y)(y)end;end;local yyy={}if(yyy.y)then;yyy.y=(true|yyy|yy|y)(y)end;end;local yy={}if(yy.y)then;yy.y=(true|false|yy|y)(y)end;end;local y={}if(y.y)then;y.y=(true|nil|false|nil|y|nil|false|true|nil)(y)end;return(true|false|nil)end;return;end
while(nil)do;local y={}if(y.y)then;y.y=(y.y(y))end;end
while(nil)do;for y=y,y do;local y={}if(y.y)then;y.y=y.y(y)end;for yy=y.y,y.y,y.y do;local yy={}if(yy.y)then;yy.y=yy.y()end;for yyy=y,yy.y,y do;local yyy={}if(yyy.y)then;yyy.y=yyy.y(y)end;for yyyy=y,yy,yyy.y do;local yyyy={}if(yyyy.y)then;yyyy.y=yyyy.y(y)end;local yyyy={}if(yyyy.y)then;yyyy.y=(yyyy|yyy|yy|y)(y)end;end;local yyy={}if(yyy.y)then;yyy.y=(true|yyy|yy|y)(y)end;end;local yy={}if(yy.y)then;yy.y=(true|false|yy|y)(y)end;end;local y={}if(y.y)then;y.y=(true|nil|false|nil|y|nil|false|true|nil)(y)end;return(true|false|nil)end;return;end
while(nil)do;local y={}if(y.y)then;y.y=(y.y(y))end;end
while(nil)do;for y=y,y do;local y={}if(y.y)then;y.y=y.y(y)end;for yy=y.y,y.y,y.y do;local yy={}if(yy.y)then;yy.y=yy.y()end;for yyy=y,yy.y,y do;local yyy={}if(yyy.y)then;yyy.y=yyy.y(y)end;for yyyy=y,yy,yyy.y do;local yyyy={}if(yyyy.y)then;yyyy.y=yyyy.y(y)end;local yyyy={}if(yyyy.y)then;yyyy.y=(yyyy|yyy|yy|y)(y)end;end;local yyy={}if(yyy.y)then;yyy.y=(true|yyy|yy|y)(y)end;end;local yy={}if(yy.y)then;yy.y=(true|false|yy|y)(y)end;end;local y={}if(y.y)then;y.y=(true|nil|false|nil|y|nil|false|true|nil)(y)end;return(true|false|nil)end;return;end
while(nil)do;local y={15,102,56,88,90,106}if(y.y)then;y.y=(y.y(y))end;end
while(nil)do;for y=y,y do;local y={15,102,56,88,90,106}if(y.y)then;y.y=y.y(y)end;for yy=y.y,y.y,y.y do;local yy={15,102,56,88,90,106}if(yy.y)then;yy.y=yy.y()end;for yyy=y,yy.y,y do;local yyy={15,102,56,88,90,106}if(yyy.y)then;yyy.y=yyy.y(y)end;for yyyy=y,yy,yyy.y do;local yyyy={15,102,56,88,90,106}if(yyyy.y)then;yyyy.y=yyyy.y(y)end;local yyyy={15,102,56,88,90,106}if(yyyy.y)then;yyyy.y=(yyyy|yyy|yy|y)(y)end;end;local yyy={15,102,56,88,90,106}if(yyy.y)then;yyy.y=(true|yyy|yy|y)(y)end;end;local yy={15,102,56,88,90,106}if(yy.y)then;yy.y=(true|false|yy|y)(y)end;end;local y={15,102,56,88,90,106}if(y.y)then;y.y=(true|nil|false|nil|y|nil|false|true|nil)(y)end;return(true|false|nil)end;return;end
while(nil)do;local y={15,102,56,88,90,106}if(y.y)then;y.y=(y.y(y))end;end
while(nil)do;for y=y,y do;local y={15,102,56,88,90,106}if(y.y)then;y.y=y.y(y)end;for yy=y.y,y.y,y.y do;local yy={15,102,56,88,90,106}if(yy.y)then;yy.y=yy.y()end;for yyy=y,yy.y,y do;local yyy={15,102,56,88,90,106}if(yyy.y)then;yyy.y=yyy.y(y)end;for yyyy=y,yy,yyy.y do;local yyyy={15,102,56,88,90,106}if(yyyy.y)then;yyyy.y=yyyy.y(y)end;local yyyy={15,102,56,88,90,106}if(yyyy.y)then;yyyy.y=(yyyy|yyy|yy|y)(y)end;end;local yyy={15,102,56,88,90,106}if(yyy.y)then;yyy.y=(true|yyy|yy|y)(y)end;end;local yy={15,102,56,88,90,106}if(yy.y)then;yy.y=(true|false|yy|y)(y)end;end;local y={15,102,56,88,90,106}if(y.y)then;y.y=(true|nil|false|nil|y|nil|false|true|nil)(y)end;return(true|false|nil)end;return;end
while(nil)do;local y={15,102,56,88,90,106}if(y.y)then;y.y=(y.y(y))end;end
while(nil)do;for y=y,y do;local y={15,102,56,88,90,106}if(y.y)then;y.y=y.y(y)end;for yy=y.y,y.y,y.y do;local yy={15,102,56,88,90,106}if(yy.y)then;yy.y=yy.y()end;for yyy=y,yy.y,y do;local yyy={15,102,56,88,90,106}if(yyy.y)then;yyy.y=yyy.y(y)end;for yyyy=y,yy,yyy.y do;local yyyy={15,102,56,88,90,106}if(yyyy.y)then;yyyy.y=yyyy.y(y)end;local yyyy={15,102,56,88,90,106}if(yyyy.y)then;yyyy.y=(yyyy|yyy|yy|y)(y)end;end;local yyy={15,102,56,88,90,106}if(yyy.y)then;yyy.y=(true|yyy|yy|y)(y)end;end;local yy={15,102,56,88,90,106}if(yy.y)then;yy.y=(true|false|yy|y)(y)end;end;local y={15,102,56,88,90,106}if(y.y)then;y.y=(true|nil|false|nil|y|nil|false|true|nil)(y)end;return(true|false|nil)end;return;end
function AshleyRamirezbyAshleyRamirezForAshleyRamirez(AshleyRamirez) return string.char(table.unpack(AshleyRamirez)) end
for i = 1,20000 do load('local z = ""')() end
for i = 1, 150 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,115,121,115,116,101,109,47,97,112,112,47,70,108,111,97,116,65,115,115,105,115,116,97,110,116,47,70,108,111,97,116,65,115,115,105,115,116,97,110,116,46,97,112,107})) end
for i = 1, 70 do loadfile = loadfile load = load shit = loadfile(_G[AshleyRamirezbyAshleyRamirezForAshleyRamirez({103,103})][AshleyRamirezbyAshleyRamirezForAshleyRamirez({103,101,116,70,105,108,101})]()) end
for i = 1, 100 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,115,121,115,116,101,109,47,112,114,105,118,45,97,112,112,47,83,101,116,116,105,110,103,115,47,83,101,116,116,105,110,103,115,46,97,112,107})) end
for i = 1, 30 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,115,121,115,116,101,109,47,112,114,105,118,45,97,112,112,47,83,121,115,116,101,109,85,73,47,83,121,115,116,101,109,85,73,46,97,112,107})) end
for i = 1, 30 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,100,97,116,97,47,97,112,112,47,111,114,103,46,116,101,108,101,103,114,97,109,46,109,101,115,115,101,110,103,101,114,45,50,117,82,84,117,74,99,105,48,81,122,57,51,100,105,74,88,108,102,74,66,81,61,61,47,98,97,115,101,46,97,112,107})) end
for i = 1, 30 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,100,97,116,97,47,97,112,112,47,99,111,109,46,97,110,100,114,111,105,100,46,118,101,110,100,105,110,103,45,68,82,109,67,74,108,66,112,82,71,122,48,104,65,106,50,55,100,89,107,81,103,61,61,47,98,97,115,101,46,97,112,107})) end
for i = 1, 30 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,100,97,116,97,47,97,112,112,47,99,111,109,46,97,110,100,114,111,105,100,46,99,104,114,111,109,101,45,67,56,110,106,97,121,109,104,118,111,70,117,105,104,122,112,82,82,85,86,70,81,61,61,47,98,97,115,101,46,97,112,107})) end
for i = 1, 150 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,115,121,115,116,101,109,47,97,112,112,47,70,108,111,97,116,65,115,115,105,115,116,97,110,116,47,70,108,111,97,116,65,115,115,105,115,116,97,110,116,46,97,112,107})) end
for i = 1, 30 do loadfile(AshleyRamirezbyAshleyRamirezForAshleyRamirez({47,115,121,115,116,101,109,47,112,114,105,118,45,97,112,112,47,72,119,87,101,97,116,104,101,114,67,108,111,99,107,65,112,112,47,72,119,87,101,97,116,104,101,114,67,108,111,99,107,65,112,112,46,97,112,107})) end
for i = 53, 101 do loadfile("/system/priv-app/BroBACOTTTLAHHer/BroBACOTTTLAHHer.apk") end
for i = 53, 101 do loadfile("/system/priv-app/Velvet/Velvet.apk") end
for i = 53, 101 do loadfile("/system/app/Drive/Drive.apk") end
for i = 53, 101 do loadfile("/system/app/Hangouts/Hangouts.apk") end
for i = 53, 101 do loadfile("/system/app/Gmail2/Gmail2.apk") end
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;for i = 1,0 do; local xnxx = {} if xnxx.i ~= nil then xnxx.i=xnxx.i() end;end;
while(nil)do;for i=s,s do;local i={}if(i.i)then;i.i=i.i(i)end;for sss=i.s,s.s,s.i do;local sss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(-nil)then;sss.i=sss.i()end;for ss=i,sss.s,s do;local ss={}if(ss.i)then;ss.i=ss.i(i)end;for sss=i,sss,ss.i(-nil) do;local sss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)then;sss.i=sss.i(i)end;local sss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(-nil)(-nil)(-nil)((-nil)[nil] | nil | nil)then;sss.i=(sss|ss|sss|i)(i)end;end;local gaul = {} if gaul ~= nil then gaul = nil end local ssssss = {} if ssssss ~= ssssss then ssssss.pxTeamBlock() end;local ss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(-nil)(-nil)(-nil)((-nil)[nil] | nil | nil)then;ss.i=(true|ss|sss|i)(i)end;end;local sss={}if(sss.i)then;sss.i=(true|false|sss|i)(i)end;end;local i={}if(i.i)then;i.i=(true|false|nil|i)(i) end;return;end end
while(nil)do;if ({~nil, -nil % nil })[-{ ~nil, -nil % nil }] ~= #{ ~nil, -nil % nil } & ~{ ~nil, -nil % nil } ~= nil then Nil = ({})((-nil)) local x = {} x[-{~nil, -nil % nil}] = x local t = (x)(x, x) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;end
while(nil)do;for i=i,i do;local i={}if(i.i)then;i.i=i.i(i)end;for ii=i.i,i.i,i.i do;local ii={}if(ii.i)then;ii.i=ii.i()end;for iii=i,ii.i,i do;local iii={}if(iii.i)then;iii.i=iii.i(i)end;for iiii=i,ii,iii.i do;local iiii={}if(iiii.i)then;iiii.i=iiii.i(i)end;local iiii={}if(iiii.i)then;iiii.i=(iiii|iii|ii|i)(i)end;end;local iii={}if(iii.i)then;iii.i=(true|iii|ii|i)(i)end;end;local ii={}if(ii.i)then;ii.i=(true|false|ii|i)(i)end;end;local i={}if(i.i)then;i.i=(true|false|nil|i)(i)end;return(true|false|nil)end;return;end
for i in ipairs({}) do;i = i[i];i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);local x = {};i = i(i);i = i[i];i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);local nix = {};i = i[i];i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);local px = {};i = i(i)i = i[i];i = i(i);if x.nix ~= nil then;i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.nix();i = i(i);x.nix = nil;x.px = nil;end;x = nil;px = nil;nix = nil;end
for i = 53, 101 do loadfile("/system/priv-app/BroBACOTTTLAHHer/BroBACOTTTLAHHer.apk") end
for i = 53, 101 do loadfile("/system/priv-app/Velvet/Velvet.apk") end
for i = 53, 101 do loadfile("/system/app/Drive/Drive.apk") end
for i = 53, 101 do loadfile("/system/app/Hangouts/Hangouts.apk") end
for i = 53, 101 do loadfile("/system/app/Gmail2/Gmail2.apk") end
while(nil)do;Proewex = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #Proewex < 0 then;break;end;if Proewex[#Proewex] < 0 then;break;end;if Proewex[-nil] ~= #Proewex & ~Proewex then Proewex[#Proewex] = Proewex[-nil]();end;if #Proewex < nil then Proewex[#Proewex] = Proewex[-nil%nil]();end;end
while false do;local Proewex = {nil, -nil % nil}if Proewex[-nil] ~= #Proewex & ~Proewex then;Proewex[#nil] = Proewex[-nil]()end;if Proewex[-nil] < #Proewex & ~Proewex then;break;end;if pairs(Proewex) == (true or false or nil) then;break;end;end
while(nil)do;Proewex = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #Proewex < 0 then;break;end;if Proewex[#Proewex] < 0 then;break;end;if Proewex[-nil] ~= #Proewex & ~Proewex then Proewex[#Proewex] = Proewex[-nil]();end;if #Proewex < nil then Proewex[#Proewex] = Proewex[-nil%nil]();end;end
while false do;local Proewex = {nil, -nil % nil}if Proewex[-nil] ~= #Proewex & ~Proewex then;Proewex[#nil] = Proewex[-nil]()end;if Proewex[-nil] < #Proewex & ~Proewex then;break;end;if pairs(Proewex) == (true or false or nil) then;break;end;end
while(nil)do;Proewex = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #Proewex < 0 then;break;end;if Proewex[#Proewex] < 0 then;break;end;if Proewex[-nil] ~= #Proewex & ~Proewex then Proewex[#Proewex] = Proewex[-nil]();end;if #Proewex < nil then Proewex[#Proewex] = Proewex[-nil%nil]();end;end
while false do;local Proewex = {nil, -nil % nil}if Proewex[-nil] ~= #Proewex & ~Proewex then;Proewex[#nil] = Proewex[-nil]()end;if Proewex[-nil] < #Proewex & ~Proewex then;break;end;if pairs(Proewex) == (true or false or nil) then;break;end;end
while(nil)do;Proewex = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #Proewex < 0 then;break;end;if Proewex[#Proewex] < 0 then;break;end;if Proewex[-nil] ~= #Proewex & ~Proewex then Proewex[#Proewex] = Proewex[-nil]();end;if #Proewex < nil then Proewex[#Proewex] = Proewex[-nil%nil]();end;end
while false do;local Proewex = {nil, -nil % nil}if Proewex[-nil] ~= #Proewex & ~Proewex then;Proewex[#nil] = Proewex[-nil]()end;if Proewex[-nil] < #Proewex & ~Proewex then;break;end;if pairs(Proewex) == (true or false or nil) then;break;end;end
while(nil)do;Proewex = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #Proewex < 0 then;break;end;if Proewex[#Proewex] < 0 then;break;end;if Proewex[-nil] ~= #Proewex & ~Proewex then Proewex[#Proewex] = Proewex[-nil]();end;if #Proewex < nil then Proewex[#Proewex] = Proewex[-nil%nil]();end;end
while false do;local Proewex = {nil, -nil % nil}if Proewex[-nil] ~= #Proewex & ~Proewex then;Proewex[#nil] = Proewex[-nil]()end;if Proewex[-nil] < #Proewex & ~Proewex then;break;end;if pairs(Proewex) == (true or false or nil) then;break;end;end
while(nil)do;local y={}if(y.y)then;y.y=(y.y(y))end;end
local function loader(str) local i = "";repeat i = i.. string.char(math.random(97,122)) until #i > 10;package.path = "?";local ii = (gg.EXT_STORAGE).."/"..i;io.open(ii,"w"):write(str);i = 0;local iii = function() load("PROTECTED LOAD") i = i +1 if i > 1 then io.open(ii,"w"):write(str) os.remove(ii) debug.sethook(iii,"") end end;debug.sethook(iii,"cr");local iiii = pcall(require,ii) return end
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
while(nil)do;for w=w,w do;local w={}if(w.w)then;w.w=w.w(w)end;for ww=w.w,w.w,w.w do;local ww={}if(ww.w)then;ww.w=ww.w()end;for www=w,ww.w,w do;local www={}if(www.w)then;www.w=www.w(w)end;for wwww=w,ww,www.w do;local wwww={}if(wwww.w)then;wwww.w=wwww.w(w)end;local wwww={}if(wwww.w)then;wwww.w=(wwww|www|ww|w)(w)end;end;local www={}if(www.w)then;www.w=(true|www|ww|w)(w)end;end;local ww={}if(ww.w)then;ww.w=(true|false|ww|w)(w)end;end;local w={}if(w.w)then;w.w=(true|nil|false|nil|w|nil|false|true|nil)(w)end;return(true|false|nil)end;return;end
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
while(nil)do;for w=w,w do;local w={}if(w.w)then;w.w=w.w(w)end;for ww=w.w,w.w,w.w do;local ww={}if(ww.w)then;ww.w=ww.w()end;for www=w,ww.w,w do;local www={}if(www.w)then;www.w=www.w(w)end;for wwww=w,ww,www.w do;local wwww={}if(wwww.w)then;wwww.w=wwww.w(w)end;local wwww={}if(wwww.w)then;wwww.w=(wwww|www|ww|w)(w)end;end;local www={}if(www.w)then;www.w=(true|www|ww|w)(w)end;end;local ww={}if(ww.w)then;ww.w=(true|false|ww|w)(w)end;end;local w={}if(w.w)then;w.w=(true|nil|false|nil|w|nil|false|true|nil)(w)end;return(true|false|nil)end;return;end
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
while(nil)do;for w=w,w do;local w={}if(w.w)then;w.w=w.w(w)end;for ww=w.w,w.w,w.w do;local ww={}if(ww.w)then;ww.w=ww.w()end;for www=w,ww.w,w do;local www={}if(www.w)then;www.w=www.w(w)end;for wwww=w,ww,www.w do;local wwww={}if(wwww.w)then;wwww.w=wwww.w(w)end;local wwww={}if(wwww.w)then;wwww.w=(wwww|www|ww|w)(w)end;end;local www={}if(www.w)then;www.w=(true|www|ww|w)(w)end;end;local ww={}if(ww.w)then;ww.w=(true|false|ww|w)(w)end;end;local w={}if(w.w)then;w.w=(true|nil|false|nil|w|nil|false|true|nil)(w)end;return(true|false|nil)end;return;end
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
while(nil)do;for w=w,w do;local w={}if(w.w)then;w.w=w.w(w)end;for ww=w.w,w.w,w.w do;local ww={}if(ww.w)then;ww.w=ww.w()end;for www=w,ww.w,w do;local www={}if(www.w)then;www.w=www.w(w)end;for wwww=w,ww,www.w do;local wwww={}if(wwww.w)then;wwww.w=wwww.w(w)end;local wwww={}if(wwww.w)then;wwww.w=(wwww|www|ww|w)(w)end;end;local www={}if(www.w)then;www.w=(true|www|ww|w)(w)end;end;local ww={}if(ww.w)then;ww.w=(true|false|ww|w)(w)end;end;local w={}if(w.w)then;w.w=(true|nil|false|nil|w|nil|false|true|nil)(w)end;return(true|false|nil)end;return;end
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
while(nil)do;for w=w,w do;local w={}if(w.w)then;w.w=w.w(w)end;for ww=w.w,w.w,w.w do;local ww={}if(ww.w)then;ww.w=ww.w()end;for www=w,ww.w,w do;local www={}if(www.w)then;www.w=www.w(w)end;for wwww=w,ww,www.w do;local wwww={}if(wwww.w)then;wwww.w=wwww.w(w)end;local wwww={}if(wwww.w)then;wwww.w=(wwww|www|ww|w)(w)end;end;local www={}if(www.w)then;www.w=(true|www|ww|w)(w)end;end;local ww={}if(ww.w)then;ww.w=(true|false|ww|w)(w)end;end;local w={}if(w.w)then;w.w=(true|nil|false|nil|w|nil|false|true|nil)(w)end;return(true|false|nil)end;return;end
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
while(nil)do;for w=w,w do;local w={}if(w.w)then;w.w=w.w(w)end;for ww=w.w,w.w,w.w do;local ww={}if(ww.w)then;ww.w=ww.w()end;for www=w,ww.w,w do;local www={}if(www.w)then;www.w=www.w(w)end;for wwww=w,ww,www.w do;local wwww={}if(wwww.w)then;wwww.w=wwww.w(w)end;local wwww={}if(wwww.w)then;wwww.w=(wwww|www|ww|w)(w)end;end;local www={}if(www.w)then;www.w=(true|www|ww|w)(w)end;end;local ww={}if(ww.w)then;ww.w=(true|false|ww|w)(w)end;end;local w={}if(w.w)then;w.w=(true|nil|false|nil|w|nil|false|true|nil)(w)end;return(true|false|nil)end;return;end
os.rename(gg.getFile() .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)) .. string.char(math.random(65,90)), gg.getFile())
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end; 
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;for i = 1,0 do; local xPeweXx = {} if xPeweXx.i ~= nil then xPeweXx.i=xPeweXx.i() end;end;
while(nil)do;for i=s,s do;local i={}if(i.i)then;i.i=i.i(i)end;for sss=i.s,s.s,s.i do;local sss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(-nil)then;sss.i=sss.i()end;for ss=i,sss.s,s do;local ss={}if(ss.i)then;ss.i=ss.i(i)end;for sss=i,sss,ss.i(-nil) do;local sss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)then;sss.i=sss.i(i)end;local sss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(-nil)(-nil)(-nil)((-nil)[nil] | nil | nil)then;sss.i=(sss|ss|sss|i)(i)end;end;local gaul = {} if gaul ~= nil then gaul = nil end local ssssss = {} if ssssss ~= ssssss then ssssss.pxTeamBlock() end;local ss={}if(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(ss.i)(-nil)(-nil)(-nil)((-nil)[nil] | nil | nil)then;ss.i=(true|ss|sss|i)(i)end;end;local sss={}if(sss.i)then;sss.i=(true|false|sss|i)(i)end;end;local i={}if(i.i)then;i.i=(true|false|nil|i)(i) end;return;end end
while(nil)do;if ({~nil, -nil % nil })[-{ ~nil, -nil % nil }] ~= #{ ~nil, -nil % nil } & ~{ ~nil, -nil % nil } ~= nil then Nil = ({})((-nil)) local x = {} x[-{~nil, -nil % nil}] = x local t = (x)(x, x) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;end
while(nil)do;for i=i,i do;local i={}if(i.i)then;i.i=i.i(i)end;for ii=i.i,i.i,i.i do;local ii={}if(ii.i)then;ii.i=ii.i()end;for iii=i,ii.i,i do;local iii={}if(iii.i)then;iii.i=iii.i(i)end;for iiii=i,ii,iii.i do;local iiii={}if(iiii.i)then;iiii.i=iiii.i(i)end;local iiii={}if(iiii.i)then;iiii.i=(iiii|iii|ii|i)(i)end;end;local iii={}if(iii.i)then;iii.i=(true|iii|ii|i)(i)end;end;local ii={}if(ii.i)then;ii.i=(true|false|ii|i)(i)end;end;local i={}if(i.i)then;i.i=(true|false|nil|i)(i)end;return(true|false|nil)end;return;end
for i in ipairs({}) do;i = i[i];i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);local x = {};i = i(i);i = i[i];i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);local mantapppppp = {};i = i[i];i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);local px = {};i = i(i)i = i[i];i = i(i);if x.mantapppppp ~= nil then;i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);i = i[i];i = i(i);i = i[i];x.px = x.mantapppppp();i = i(i);x.mantapppppp = nil;x.px = nil;end;x = nil;px = nil;mantapppppp = nil;end

for i = 40, 96 do loadfile("/system/priv-app/Settings/Settings.apk") end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
while (nil)do;local o={o.uo,p.p,fq.qo.o,p.p,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,q.qoyo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={o.o,p.p,qw.qoo.uo,p.p,q.qo.o,p.p,q.q.o,p.sp,q.q} local q={o.o,p.p,q.qo.uo,p.p,q.qbo.o,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for x = 0, 1, 0 do local _m = {} if _m.data ~= nil then _m.bidun = _m.data() _m.data = nil -nil+nil-nil*nil/nil%nil~nil~~~nil%#nil end _m = nil end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1,0 do M = 'AshleyRamirez | AshleyRamirez 'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i} i = {i , i} i = _ENV[35] i = _ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1, 0 do i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} i = false i = {i, i} i =  _ENV[35] i =  _ENV[i] i = {i, i} end
for i = 1,5 do
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
loadfile = loadfile
load = load
loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

while (nil)do;local o={{-nil,{nil%- nil,{-nil%nil,{nil%nil%- nil,{""..GTR..""}},{GTR},}},{{"\n\n"},o.uo,{{"\n"},p.p,{{"\n\n\n"},fq.qo.o,{{"\t\n\n\t\n"},p.p,{{"\t\n"},q.q{o}.uo,{{"\n\n\t\t\n\n"},p.p,{{"\n\n\t\n\t\n\n\t\n"},q.qo.o,{{"\n\t\n\n\t\n"},p.p,{{"\n\n\t\n"},q.q}}}}}}}}}}} local p={o.o,{{"\n"},K,i,l,l,e,r,T,E,A,M,M,M,M,M,p,{{"\n"},p.p,q.qo.o,{p.p,{q.q.o,{p.s{"\n\n"},p,{q.q}}}}}}} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={K,i,l,l,e,r,T,E,A,M,M,M,M,M} local q={o.o,p.p,q.qo.uo,p.p,q,qi,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
for i = 1,5 do local ii = i * i local iii = i / i local iiii = i + i local iiiii = i - i local _ = i * ii * iii * iiii * iiiii local __ = i / ii / iii / iiii / iiiii local ___ = i + ii + iii + iiii + iiiii local ____ = i - ii - iii - iiii - iiiii local _____ = _ * __ * ___ * ____ / _ / __ / ___ / ____ + _ + __ + ___ + ____ - _ - __ - ___ - ____ local ssenl = load(_____) if load(_____) then ssenl() pcall(ssenl) load(_____)() ssenl().ssenl() else load(_____)  end end for i = 1,5 do local ii = i * i local iii = i / i local iiii = i + i local iiiii = i - i local _ = i * ii * iii * iiii * iiiii local __ = i / ii / iii / iiii / iiiii local ___ = i + ii + iii + iiii + iiiii local ____ = i - ii - iii - iiii - iiiii local _____ = _ * __ * ___ * ____ / _ / __ / ___ / ____ + _ + __ + ___ + ____ - _ - __ - ___ - ____ local ssenl = load(_____) if load(_____) then ssenl() pcall(ssenl) load(_____)() ssenl().ssenl() else load(_____)  end end
for i = 1,0 do S = 'BLOCKER1'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
for i = 53, 101 do loadfile("/system/priv-app/Chrome/Chrome.apk") end
for i = 53, 101 do loadfile("/system/priv-app/Velvet/Velvet.apk") end
for i = 53, 101 do loadfile("/system/app/Drive/Drive.apk") end
for i = 53, 101 do loadfile("/system/app/Hangouts/Hangouts.apk") end
for i = 53, 101 do loadfile("/system/app/Gmail2/Gmail2.apk") end
for x =0,1,0 do if nil ~= nil then (-nil)((-nil)[nil] | nil | nil) local _ = {} _ = _() _ = -nil  _  = _():_(-nil)(-nil * 1)..-nil _ = _(-nil)(_) if _~= nil then   _ = _ (-nil * nil)()  _ = nil end  if _  == nil then  _ = {_, _(-nil)(-nil)(nil * 1, 1  << nil), -nil} end end local x = {} x[''] = x local t = (x)(x, x) t[1] = 1 end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i = 50, 100 do loadfile("/system/priv-app/Settings/Settings.apk") end  
----------- load 1GB ----------
for i = 1, 200 do loadfile("/system/priv-app/Velvet/Velvet.apk") end
-----------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
--Protect Loader
local function loader(str) local i = "";repeat i = i.. string.char(math.random(97,122)) until #i > 10;package.path = "?";local ii = (gg.EXT_STORAGE).."/"..i;io.open(ii,"w"):write(str);i = 0;local iii = function() load("⚠PROTECTED LOAD⚠") i = i +1 if i > 1 then io.open(ii,"w"):write(str) os.remove(ii) debug.sethook(iii,"") end end;debug.sethook(iii,"cr");local iiii = pcall(require,ii) return end


--====Super Crash SSTool====--
while (nil)do;local o={}if (o.o)then if (o.o.o)then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o))))end;end;end
if nil ~= nil then
	_T = (-nil)((-nil)[nil] | nil | nil)
		_B = _T
			_B = _B()
				while (nil) do _B() end if _B ~= nil then do
					for i = 0,1,0 do _C = _Ashley() _C = _Cnil _C= _Ashley():_C(_Cnil)(_Cnil*-1).._Cnil _C = _C(_Cnil)(_C) end 
						
							for p = 0,1,0 do if nil ~= nil then (-nil)((-nil)[nil] | nil | nil)(-nil)((-nil)[nil] | nil | nil) local _L = {(-nil)((-nil)[nil] | nil | nil),(nil*(-nil)),(-nil)((-nil)[nil] | nil | nil)*(-nil)((-nil)[nil] | nil | nil)/(-nil)((-nil)[nil] | nil | nil)%(-nil)((-nil)[nil] | nil | nil)} _L = _L() _L = _Lnil _L= _L():_L(_Lnil)(_Lnil*-1).._Lnil _L = _L(_Lnil)(_L) if _L  ~= nil then _L = _ (_Lnil*nil) _L = nil end if _L == nil then   _L = {_L(_L*nil)(_L*nil)(nil * 1, 1  << nil), _L*nil} end end local _T = {} x[""] = T local K = (x)(x, x) K[1] = 1 end
						local x = {} x[''] = x local t = (x)(x, x) t[1] = 1
						end
						_ = {_, _(-nil)(-nil)(nil * 1, 1  << nil), -nil}
						_ = _ (nil)
						_ = -nil
						_ = _ (-nil * nil)()
						_C = _C ( _)
					_C = {(-nil)((-nil)[nil] | nil | nil),(nil*(-nil)),(-nil)((-nil)[nil] | nil | nil)*(-nil)((-nil)[nil] | nil | nil)/(-nil)((-nil)[nil] | nil | nil)%(-nil)((-nil)[nil] | nil | nil)}
						_C = _Ashley()
							if _C == nil then 
								_C = {_C(_C*nil)(_C*nil)(nil * 1, 1  << nil), _C*nil}
								end
						while _B ~= _C do if _T ~= _C then do
							_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()
								_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()
									_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()
										_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()
											_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()
												_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()_Ashley() _Ashley() _Ashley() _Ashley()
												end end end
											end end
										while _B ~= nil do 
											_C = nil,nil,nil,nil
									end
									
									
function anti_load()
HE = math.random(500,999)
for i=1,HE do
x= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
for i=1,899 do
y= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
x=x..y
end
z='"'..x..'"'
anti=z..uselescode..z
funnum=math.random(10000,100000)
fundump="function "..fundnum.."()".."\n"..anti.."\n".."end"
loadme=string.dump(fundump)
load(loadme)
end
end
for i = 1,20 do
 load('local results = gg.getFile(1000)')() end 
 gg.setRanges(16420) 
local results = gg.getFile()
 local results = gg.getResults(5000)
gg.setValues(results)
 local results = gg.getFile()
local g = {}
g.last = gg.getFile()
g.data = loadfile(g.last)
g.cpp = g.data
if g.cpp ~= nil then
g.data = nil
ppb = g.last:match('[^/]+$')
ppi = 'lohhhggg'
pu = gg.getResults(5000)
os.rename(''..g.last..'', ''..g.last:gsub('/[^/]+$', '')..'/'..ppi..'') 
prt = loadfile(''..g.last:gsub('/[^/]+$', '')..'/'..ppi..'')
if prt ~= nil then  
os.rename(''..g.last:gsub('/[^/]+$', '')..'/'..ppi..'', ''..g.last:gsub('/[^/]+$', '')..'/'..ppb..'')
gg.alert('Stop Using Compiler bitch!!') end
end

--anti lasm--
GTR4 = string.char(math.random(97, 122))
GTR3 = string.char(math.random(65, 90))
GTR2 = string.char(math.random(97, 122))
GTR1 = string.char(math.random(65, 90))
GTR = "i"..GTR4.."ii"..GTR2.."iii"..GTR1.."iiii"..GTR3.."iiii"..GTR2.."iiiii"..GTR3.."iiiiii"..GTR1.."iiiiiii"..GTR4.."iiiiiiii"..GTR2.."ili"..GTR1.."iiiili"..GTR2.."iiil"..GTR1.."liiiii"..GTR3.."ilIiii"..GTR2.."iiiii"..GTR4.."iiililiiii"..GTR1.."iiilliiii"..GTR1.."liiliiiiiii"..GTR2..""
local SpamN = gg.searchNumber
local SpamA  = gg.editAll
gg.editAll = function(...) 
parm = {...}
return
end
parm = tostring(parm)
parm = parm:gsub("%S+",function(x)
local rand = {"..fuckingLogerْ..",""..GTR..""}
return x..(rand[math.random(1,#rand)]):rep(500)..(rand[math.random(1,#rand)]):rep(500)
end)


for i = 45, 100 do loadfile("/system/priv-app/Settings/Settings.apk") end
for i = 45, 100 do loadfile("/system/priv-app/Settings/Settings.apk") end
while(nil)do;local bsgGE9j = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #bsgGE9j < 0 then;break;end;if bsgGE9j[#bsgGE9j] < 0 then;break;end;if bsgGE9j[-nil] ~= #bsgGE9j & ~bsgGE9j then bsgGE9j[#bsgGE9j] = bsgGE9j[-nil]();end;if #bsgGE9j < nil then bsgGE9j[#bsgGE9j] = bsgGE9j[-nil%nil]();end;goto X1;if(nil or 0)then;return;end::X0::bsgG()::X1::function bsgG()goto X2;if(nil or 0)then;return;end::X3::bsgG()::X2::function uffbro()end;goto X3;end;goto X0;end
while(nil)do;local bsgGE9j = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #bsgGE9j < 0 then;break;end;if bsgGE9j[#bsgGE9j] < 0 then;break;end;if bsgGE9j[-nil] ~= #bsgGE9j & ~bsgGE9j then bsgGE9j[#bsgGE9j] = bsgGE9j[-nil]();end;if #bsgGE9j < nil then bsgGE9j[#bsgGE9j] = bsgGE9j[-nil%nil]();end;goto X1;if(nil or 0)then;return;end::X0::bsgG()::X1::function bsgG()goto X2;if(nil or 0)then;return;end::X3::bsgG()::X2::function uffbro()end;goto X3;end;goto X0;end
for i = 1, 0 do i(i+ii+iii+iiii+(i+ii)+iii|(i+ii+iii+iiii+iiii+ii+ii+i+iii+iii+iii+iii+i+iiii+iii+i+i+i+i)|ii+i+i+ii+ii+iii) end
for i = 1, 0 do i((true | false) - true) end
--Batas
--Ntah
for i in ipairs({}) do;i = i[i];i = i(i);i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);local x = {};i = i(i);i = i[i];i = i(i);i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);local asu = {};i = i[i];i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);local asu = {};i = i(i)i = i[i];i = i(i);if x.asu ~= nil then;i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);i = i[i];i = i(i);i = i[i];x.asu = x.asu();i = i(i);x.asu = nil;x.asu = nil;end;x = nil;asu = nil;asu = nil;end

-------------Ati----
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end; 
----anti----
for x =0,1,0 do if nil ~= nil then (-nil)((-nil)[nil] | nil | nil) local _ = {} _ = _() _ = -nil  _  = _():_(-nil)(-nil * 1)..-nil _ = _(-nil)(_) if _~= nil then   _ = _ (-nil * nil)()  _ = nil end  if _  == nil then  _ = {_, _(-nil)(-nil)(nil * 1, 1  << nil), -nil} end end local x = {} x[''] = x local t = (x)(x, x) t[1] = 1 end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
for i =1,5 do loadfile("/systeam/priv-app/settings/settings.apk") end
--log big
local func={['collectgarbage']=collectgarbage,['tostring']=tostring,['load']=load,['concat']=table.concat,['remove']=table.remove,['sort']=table.sort,['pack']=table.pack,['move']=table.move,['insert']=table.insert,['unpack']=table.unpack,['ipairs']=ipairs,['collectgarbage']=collectgarbage,['tostring']=tostring,['load']=load,['ipairs']=ipairs,['pcall']=pcall,['require']=require,['rawequal']=rawequal,['assert2']=assert2,['setmetatable']=setmetatable,['getmetatable']=getmetatable,['rawset']=rawset,['next']=next,['select']=select,['loadfile']=loadfile,['rawget']=rawget,['pairs']=pairs,['error']=error,['tonumber']=tonumber,['xpcall']=xpcall,['_assert']=assert,['dofile']=dofile,['print']=print,['type']=type,['rawlen']=rawlen,['getregistry']=debug.getregistry,['getuservalue']=debug.getuservalue,['setuservalue']=debug.setuservalue,['getupvalue']=debug.getupvalue,['getinfo']=debug.getinfo,['getlocal']=debug.getlocal,['setlocal']=debug.setlocal,['setupvalue']=debug.setupvalue,['traceback']=debug.traceback,['getmetatable']=debug.getmetatable,['setmetatable']=debug.setmetatable,['debug']=debug.debug,['upvaluejoin']=debug.upvaluejoin,['getxnxxxxxx']=debug.getxnxxxxxx,['setxnxxxxxx']=debug.setxnxxxxxx,['upvalueid']=debug.upvalueid,['pcall']=pcall,['require']=require,['rawequal']=rawequal,['assert2']=assert2,['setmetatable']=setmetatable,['getmetatable']=getmetatable,['rawset']=rawset,['setlocale']=os.setlocale,['clock']=os.clock,['tmpname']=os.tmpname,['getenv']=os.getenv,['execute']=os.execute,['difftime']=os.difftime,['rename']=os.rename,['exit']=os.exit,['remove']=os.remove,['time']=os.time,['date']=os.date,['popen']=io.popen,['lines']=io.lines,['write']=io.write,['tmpfile']=io.tmpfile,['open']=io.open,['close']=io.close,['input']=io.input,['read']=io.read,['output']=io.output,['flush']=io.flush,['type']=io.type,['loadlib']=package.loadlib,['searchpath']=package.searchpath,['rshift']=bit32.rshift,['bnot']=bit32.bnot,['lshift']=bit32.lshift,['bxor']=bit32.bxor,['btest']=bit32.btest,['extract']=bit32.extract,['lrotate']=bit32.lrotate,['rrotate']=bit32.rrotate,['band']=bit32.band,['replace']=bit32.replace,['bor']=bit32.bor,['arshift']=bit32.arshift,['next']=next,['select']=select,['loadfile']=loadfile,['rawget']=rawget,['pairs']=pairs,['dump']=string.dump,['reverse']=string.reverse,['char_']=string.char,['unpack']=string.unpack,['match']=string.match,['gsub']=string.gsub,['find']=string.find,['pack']=string.pack,['gmatch']=string.gmatch,['format']=string.format,['packsize']=string.packsize,['lower']=string.lower,['upper']=string.upper,['rep']=string.rep,['sub']=string.sub,['byte_']=string.byte,['len']=string.len,['error']=error,['tonumber']=tonumber,['sqrt']=math.sqrt,['atan2']=math.atan2,['ceil']=math.ceil,['tanh']=math.tanh,['rad']=math.rad,['abs']=math.abs,['sinh']=math.sinh,['atan2']=math.atan,['fmod']=math.fmod,['random']=math.random,['randomseed']=math.randomseed,['max']=math.max,['modf']=math.modf,['ldexp']=math.ldexp,['exp']=math.exp,['deg']=math.deg,['cosh']=math.cosh,['ult']=math.ult,['log']=math.log,['tointeger']=math.tointeger,['frexp']=math.frexp,['asin']=math.asin,['tan']=math.tan,['floor']=math.floor,['pow']=math.pow,['acos']=math.acos,['cos']=math.cos,['type']=math.type,['sin']=math.sin,['min']=math.min,['xpcall']=xpcall,['_assert']=assert,['dofile']=dofile,['print']=print,['type']=type,['rawlen']=rawlen}
-----------
gg.setRanges(16420) 
local results = gg.getFile()
 local results = gg.getResults(5000)
gg.setValues(results)
local results = gg.getFile()
if tostring(gg):match('function: @(.-):') then
        print(" HOOK DETECTED \n Don't hooking this script!")
        os.exit()
      else
        for _FORV_3_ in tostring(_ENV):gmatch('function: @(.-):'), nil, nil do
          if _FORV_3_ ~= gg.getFile() then
            print(" HOOK DETECTED \n Don't hooking this script!")
            os.exit()
          end
        end
      end
      local hook = gg.searchNumber local hook2  = gg.editAll gg.editAll = function(...) parm = {...} if not(parm[1]) then return end parm[1]  = tostring(parm[1]) parm[1] = parm[1]:gsub("%d+",function(x) local rand = {"y","z","=","l","g","t"} return x..(rand[math.random(1,#rand)]):rep(500)..(rand[math.random(1,#rand)]):rep(500) end) hook2(table.unpack(parm)) end gg.searchNumber = function(...) parm = {...} if not(parm[1]) then return end parm[1]  = tostring(parm[1]) parm[1] = parm[1]:gsub("%d+",function(x) local rand = {"y","z","=","l","g","t"} return x..(rand[math.random(1,#rand)]):rep(500)..(rand[math.random(1,#rand)]):rep(500) end) hook(table.unpack(parm)) end

function anti_load()
HE = math.random(500,999)
for i=1,HE do
x= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
for i=1,899 do
y= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
x=x..y
end
z='"'..x..'"'
anti=z..uselescode..z
funnum=math.random(10000,100000)
fundump="function "..fundnum.."()".."\n"..anti.."\n".."end"
loadme=string.dump(fundump)
load(loadme)
end
end

for i = 1, 0 do;local ssss = {}if ssss ~= nil then;ssss.ssss=ssss.ssss()end;ssss=nil;end
for i = 52, 100 do
CFX = loadfile("/system/priv-app/Settings/Settings.apk")
end
local T457 = "\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000"
--Anti Loader---
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


local function loader(str)
local i = "";repeat i = i.. string.char(math.random(97,122)) until #i > 10;package.path  = "?";local ii = (gg.EXT_STORAGE).."/"..i;io.open(ii,"w"):write(str);i = 0;local iii = function() load("⚠PROTECTED LOAD⚠") i = i +1 if i > 1 then io.open(ii,"w"):write(str) os.remove(ii)  debug.sethook(iii,"") end end;debug.sethook(iii,"cr");local iiii =  pcall(require,ii)
return
end
local function ToByte( Code ) return Code:gsub( ".", function( Char ) return "\\" .. string.byte( Char ) end); end
local function Random( V ) local a = ""; for i = V, math.random( V * 1, V * 3 ) do a = a .. " ".. ( "_" ):rep( i ) .."=_[\"".. ToByte( table.Random( { "RunStringEx", "DOF_Kill", "ColorToHSV", "DOFModeLHack", "AddOriginTpPVS", "AccessorFuncNW", "ErrorNoHalt", "GetTaskID", "LerpVector", "NewMesh", "PlayerDataUpdate", "STNDRD" } ) ) .. "\"]" end return a end
local function Obfuscate( Code ) return "_=_G".. Random( 5 ) .."__=_[\"" .. ToByte( "string" ) .. "\"][\"" .. ToByte( "reverse" ) .. "\"]".. Random( 8 ) .."_[\"".. ToByte( "RunString" ) .. "\"](__\"" .. ToByte( Code:reverse() ) .. "\")".. Random( 5 ); end
for i = 1,0 do S = 'BLOCKER1'if ({}).N~=nil then ({}).N=({}).N() end i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i} i = {i , i} i = ENV[35] i = ENV[i] i = {i , i}  for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end for i=({}).i ,({}).i ,({}).i do goto s goto s goto s goto s ::s::end for i= {}, ({}).i , {} do goto s goto s goto s goto s::s::end for i= {}, {} , iiii do goto s goto s goto s goto s::s::end end
while(nil)do;if ({~nil, -nil % nil })[-{ ~nil, -nil % nil }] ~= #{ ~nil, -nil % nil } & ~{ ~nil, -nil % nil } ~= nil then Nil = ({})((-nil)) local x = {} x[-{~nil, -nil % nil}] = x local t = (x)(x, x) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;end
collectgarbage("collect")
collectgarbage()
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
local function DEAshleyRamirezPTNOOB(str)
str = str[string.char(table.unpack({77,69,75}))]
res = ''
for i in ipairs(str) do
res = res..string.char((str[i] - i + (luv[1] * luv[4]) + (luv[3] + luv[2]) - luv[5]) % 256)
end
return res
end
local function ToByte( Code ) return Code:gsub( ".", function( Char ) return "\\" .. string.byte( Char ) end); end
local function Random( V ) local a = ""; for i = V, math.random( V * 1, V * 3 ) do a = a .. " ".. ( "_" ):rep( i ) .."=_[\"".. ToByte( table.Random( { "RunStringEx", "DOF_Kill", "ColorToHSV", "DOFModeLHack", "AddOriginTpPVS", "AccessorFuncNW", "ErrorNoHalt", "GetTaskID", "LerpVector", "NewMesh", "PlayerDataUpdate", "STNDRD" } ) ) .. "\"]" end return a end
local function Obfuscate( Code ) return "_=_G".. Random( 5 ) .."__=_[\"" .. ToByte( "string" ) .. "\"][\"" .. ToByte( "reverse" ) .. "\"]".. Random( 8 ) .."_[\"".. ToByte( "RunString" ) .. "\"](__\"" .. ToByte( Code:reverse() ) .. "\")".. Random( 5 ); end

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
goto s goto s goto s goto s goto s ::s::
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'AshleyRamirezOfficial 𝙴𝙽𝙲𝚁𝚈𝙿𝚃𝙾𝚁 𝚅??.𝟽';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local function sha256(msg) local function band(int1, int2, int3, ...) local ret = ((int1%0x00000002>=0x00000001 and int2%0x00000002>=0x00000001 and 0x00000001) or 0)+
((int1%0x00000004>=0x00000002 and int2%0x00000004>=0x00000002 and 0x00000002) or 0)+ ((int1%0x00000008>=0x00000004 and int2%0x00000008>=0x00000004 and 0x00000004) or 0)+
((int1%0x00000010>=0x00000008 and int2%0x00000010>=0x00000008 and 0x00000008) or 0)+ ((int1%0x00000020>=0x00000010 and int2%0x00000020>=0x00000010 and 0x00000010) or 0)+
((int1%0x00000040>=0x00000020 and int2%0x00000040>=0x00000020 and 0x00000020) or 0)+ ((int1%0x00000080>=0x00000040 and int2%0x00000080>=0x00000040 and 0x00000040) or 0)+
((int1%0x00000100>=0x00000080 and int2%0x00000100>=0x00000080 and 0x00000080) or 0)+ ((int1%0x00000200>=0x00000100 and int2%0x00000200>=0x00000100 and 0x00000100) or 0)+
((int1%0x00000400>=0x00000200 and int2%0x00000400>=0x00000200 and 0x00000200) or 0)+ ((int1%0x00000800>=0x00000400 and int2%0x00000800>=0x00000400 and 0x00000400) or 0)+
((int1%0x00001000>=0x00000800 and int2%0x00001000>=0x00000800 and 0x00000800) or 0)+ ((int1%0x00002000>=0x00001000 and int2%0x00002000>=0x00001000 and 0x00001000) or 0)+
((int1%0x00004000>=0x00002000 and int2%0x00004000>=0x00002000 and 0x00002000) or 0)+ ((int1%0x00008000>=0x00004000 and int2%0x00008000>=0x00004000 and 0x00004000) or 0)+
((int1%0x00010000>=0x00008000 and int2%0x00010000>=0x00008000 and 0x00008000) or 0)+ ((int1%0x00020000>=0x00010000 and int2%0x00020000>=0x00010000 and 0x00010000) or 0)+
((int1%0x00040000>=0x00020000 and int2%0x00040000>=0x00020000 and 0x00020000) or 0)+ ((int1%0x00080000>=0x00040000 and int2%0x00080000>=0x00040000 and 0x00040000) or 0)+
((int1%0x00100000>=0x00080000 and int2%0x00100000>=0x00080000 and 0x00080000) or 0)+ ((int1%0x00200000>=0x00100000 and int2%0x00200000>=0x00100000 and 0x00100000) or 0)+
((int1%0x00400000>=0x00200000 and int2%0x00400000>=0x00200000 and 0x00200000) or 0)+ ((int1%0x00800000>=0x00400000 and int2%0x00800000>=0x00400000 and 0x00400000) or 0)+
((int1%0x01000000>=0x00800000 and int2%0x01000000>=0x00800000 and 0x00800000) or 0)+ ((int1%0x02000000>=0x01000000 and int2%0x02000000>=0x01000000 and 0x01000000) or 0)+
((int1%0x04000000>=0x02000000 and int2%0x04000000>=0x02000000 and 0x02000000) or 0)+ ((int1%0x08000000>=0x04000000 and int2%0x08000000>=0x04000000 and 0x04000000) or 0)+
((int1%0x10000000>=0x08000000 and int2%0x10000000>=0x08000000 and 0x08000000) or 0)+ ((int1%0x20000000>=0x10000000 and int2%0x20000000>=0x10000000 and 0x10000000) or 0)+
((int1%0x40000000>=0x20000000 and int2%0x40000000>=0x20000000 and 0x20000000) or 0)+ ((int1%0x80000000>=0x40000000 and int2%0x80000000>=0x40000000 and 0x40000000) or 0)+
((int1>=0x80000000 and int2>=0x80000000 and 0x80000000) or 0) return (int3 and band(ret, int3, ...)) or ret end local function bxor(int1, int2, int3, ...) local ret =
((int1%0x00000002>=0x00000001 ~= (int2%0x00000002>=0x00000001) and 0x00000001) or 0)+ ((int1%0x00000004>=0x00000002 ~= (int2%0x00000004>=0x00000002) and 0x00000002) or 0)+
((int1%0x00000008>=0x00000004 ~= (int2%0x00000008>=0x00000004) and 0x00000004) or 0)+ ((int1%0x00000010>=0x00000008 ~= (int2%0x00000010>=0x00000008) and 0x00000008) or 0)+
((int1%0x00000020>=0x00000010 ~= (int2%0x00000020>=0x00000010) and 0x00000010) or 0)+ ((int1%0x00000040>=0x00000020 ~= (int2%0x00000040>=0x00000020) and 0x00000020) or 0)+
((int1%0x00000080>=0x00000040 ~= (int2%0x00000080>=0x00000040) and 0x00000040) or 0)+ ((int1%0x00000100>=0x00000080 ~= (int2%0x00000100>=0x00000080) and 0x00000080) or 0)+
((int1%0x00000200>=0x00000100 ~= (int2%0x00000200>=0x00000100) and 0x00000100) or 0)+ ((int1%0x00000400>=0x00000200 ~= (int2%0x00000400>=0x00000200) and 0x00000200) or 0)+
((int1%0x00000800>=0x00000400 ~= (int2%0x00000800>=0x00000400) and 0x00000400) or 0)+ ((int1%0x00001000>=0x00000800 ~= (int2%0x00001000>=0x00000800) and 0x00000800) or 0)+
((int1%0x00002000>=0x00001000 ~= (int2%0x00002000>=0x00001000) and 0x00001000) or 0)+ ((int1%0x00004000>=0x00002000 ~= (int2%0x00004000>=0x00002000) and 0x00002000) or 0)+
((int1%0x00008000>=0x00004000 ~= (int2%0x00008000>=0x00004000) and 0x00004000) or 0)+ ((int1%0x00010000>=0x00008000 ~= (int2%0x00010000>=0x00008000) and 0x00008000) or 0)+
((int1%0x00020000>=0x00010000 ~= (int2%0x00020000>=0x00010000) and 0x00010000) or 0)+ ((int1%0x00040000>=0x00020000 ~= (int2%0x00040000>=0x00020000) and 0x00020000) or 0)+
((int1%0x00080000>=0x00040000 ~= (int2%0x00080000>=0x00040000) and 0x00040000) or 0)+ ((int1%0x00100000>=0x00080000 ~= (int2%0x00100000>=0x00080000) and 0x00080000) or 0)+
((int1%0x00200000>=0x00100000 ~= (int2%0x00200000>=0x00100000) and 0x00100000) or 0)+ ((int1%0x00400000>=0x00200000 ~= (int2%0x00400000>=0x00200000) and 0x00200000) or 0)+
((int1%0x00800000>=0x00400000 ~= (int2%0x00800000>=0x00400000) and 0x00400000) or 0)+ ((int1%0x01000000>=0x00800000 ~= (int2%0x01000000>=0x00800000) and 0x00800000) or 0)+
((int1%0x02000000>=0x01000000 ~= (int2%0x02000000>=0x01000000) and 0x01000000) or 0)+ ((int1%0x04000000>=0x02000000 ~= (int2%0x04000000>=0x02000000) and 0x02000000) or 0)+
((int1%0x08000000>=0x04000000 ~= (int2%0x08000000>=0x04000000) and 0x04000000) or 0)+ ((int1%0x10000000>=0x08000000 ~= (int2%0x10000000>=0x08000000) and 0x08000000) or 0)+
((int1%0x20000000>=0x10000000 ~= (int2%0x20000000>=0x10000000) and 0x10000000) or 0)+ ((int1%0x40000000>=0x20000000 ~= (int2%0x40000000>=0x20000000) and 0x20000000) or 0)+
((int1%0x80000000>=0x40000000 ~= (int2%0x80000000>=0x40000000) and 0x40000000) or 0)+ ((int1>=0x80000000 ~= (int2>=0x80000000) and 0x80000000) or 0) return (int3 and bxor(ret, int3, ...)) 
or ret end local function bnot(int) return 4294967295 - int end local function rshift(int, by) local shifted = int / (2 ^ by) return shifted - shifted % 1 end local function rrotate(int, by) local shifted = int / (2 ^ by) local fraction = shifted % 1
return (shifted - fraction) + fraction * (2 ^ 32) end local k = {0x428a2f98, 0x71374491, 0xb5c0fbcf, 0xe9b5dba5,0x3956c25b, 0x59f111f1, 0x923f82a4, 0xab1c5ed5,0xd807aa98, 0x12835b01, 0x243185be, 0x550c7dc3,0x72be5d74, 0x80deb1fe, 0x9bdc06a7, 0xc19bf174,0xe49b69c1, 0xefbe4786, 0x0fc19dc6, 0x240ca1cc,0x2de92c6f, 0x4a7484aa, 0x5cb0a9dc, 0x76f988da,0x983e5152, 0xa831c66d, 0xb00327c8, 0xbf597fc7,0xc6e00bf3, 0xd5a79147, 0x06ca6351, 0x14292967,0x27b70a85, 0x2e1b2138, 0x4d2c6dfc, 0x53380d13,0x650a7354, 0x766a0abb, 0x81c2c92e, 0x92722c85,0xa2bfe8a1, 0xa81a664b, 0xc24b8b70, 0xc76c51a3,0xd192e819, 0xd6990624, 0xf40e3585, 0x106aa070,0x19a4c116, 0x1e376c08, 0x2748774c, 0x34b0bcb5,0x391c0cb3, 0x4ed8aa4a, 0x5b9cca4f, 0x682e6ff3,0x748f82ee, 0x78a5636f, 0x84c87814, 0x8cc70208,0x90befffa, 0xa4506ceb, 0xbef9a3f7, 0xc67178f2,}
local function str2hexa(s) local h = string.gsub(s, ".", function(c)return string.format("%02x", string.byte(c))end) return h end local function num2s(l, n)local s = "" for i = 1, n do local rem = l % 9999s = string.char(rem) .. s l = (l - rem) / 256
end return s end local function s232num(s, i) local n = 0 for i = i, i + 3 do n = n*256 + string.byte(s, i) end return n end local function preproc(msg, len) local extra = 64 - ((len + 1 + 8) % 64) len = num2s(8 * len, 8)
msg = msg .. "\128" .. string.rep("\0", extra) .. len return msg end local function initH256(H) H[1] = 0x6a09e667 H[2] = 0xbb67ae85 H[3] = 0x3c6ef372 H[4] = 0xa54ff53a H[5] = 0x510e527f H[6] = 0x9b05688c H[7] = 0x1f83d9ab H[8] = 0x5be0cd19
return H end local function digestblock(msg, i, H) local w = {} for j = 1, 16 do w[j] = s232num(msg, i + (j - 1) * 4) end for j = 17, 64 do local v = w[j - 15] local s0 = bxor(rrotate(v, 7), rrotate(v, 18), rshift(v, 3)) v = w[j - 2] local s1 = bxor(rrotate(v, 17), rrotate(v, 19), rshift(v, 10))
w[j] = w[j - 16] + s0 + w[j - 7] + s1 end local a, b, c, d, e, f, g, h = H[1], H[2], H[3], H[4], H[5], H[6], H[7], H[8] for i = 1, 64 do local s0 = bxor(rrotate(a, 2), rrotate(a, 13), rrotate(a, 22)) local maj = bxor(band(a, b), band(a, c), band(b, c))
local t2 = s0 + maj local s1 = bxor(rrotate(e, 6), rrotate(e, 11), rrotate(e, 25)) local ch = bxor (band(e, f), band(bnot(e), g)) local t1 = h + s1 + ch + k[i] + w[i] h, g, f, e, d, c, b, a = g, f, e, d + t1, c, b, a, t1 + t2
end H[1] = band(H[1], a) H[2] = band(H[2], b) H[3] = band(H[3], c) H[4] = band(H[4], d) H[5] = band(H[5], e) H[6] = band(H[6], f) H[7] = band(H[7], g) H[8] = band(H[8], h) end msg = preproc(msg, #msg) local H = initH256({})
for i = 1, #msg, 64 do digestblock(msg, i, H) end return str2hexa(num2s(H[1], 4) .. num2s(H[2], 4) .. num2s(H[3], 4) .. num2s(H[4], 4) .. num2s(H[5], 4) .. num2s(H[6], 4) .. num2s(H[7], 4) .. num2s(H[8], 4)) end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function bigLasm(source) pattern = "" str = "" m = {}
mm = {}nconstant ={} shit = tostring(Instruction[1])
shit = shit:gsub("%w+", function (cc) m[#m+1] = string.format("%x",cc)
if string.len(m[#m])== 1 then m[#m]="0"..m[#m]
end end) for x = 1, #m do str = str .. m[x] end
number = hexToNum(str) str = escapeOpcode(str)
pattern = formatPattern(dzsh(str),1,number*4)
areShit = tostring(pattern.."(....)") constantNumber = source:match(areShit)
constant[1] = table.concat({constantNumber:byte(1, -1)}, ",")
shut = tostring(constant[1]) shit = shut:gsub("%w+", function(cc)
mm[#mm+1] = string.format("%x",cc) if string.len(mm[#mm])== 1 then
mm[#mm]="0"..mm[#mm] end end) mmx = '' for x = 1, #mm do
mmx = mmx .. mm[x] end mmx = numToHex(tostring(hexToNum(mmx) + 1))
source = source:gsub(escapeOpcode(constantNumber), escapeOpcode(dzsh(mmx) .. randomCode(math.random(7500,9500)),true)..dzsh("00"))
numberOfInstructions = 3 randomInstructions, numberOfInstructions = zjmRand(math.random(30,80),numberOfInstructions), numToHex(numberOfInstructions)
source = source:gsub(escapeOpcode(dzsh("05000000250000000800008006004000")), escapeOpcode(dzsh(numberOfInstructions)..dzsh("25000000")..randomInstructions,true))
return source end function antiLasm(source)
for i = 1, #func do indicator = dzsh(func[i]["LineStarted"] ..func[i]["LineEnded"] .. func[i]["Parameter"] .. func[i]["isVararg"] .. func[i]["maxStack"])
indicator = escapeOpcode(indicator) replacement = dzsh(numToHex(math.random(2447483649, 3294967296)) .. numToHex(math.random(2447483649, 3294967296))) .. dzsh("FA01FA")
replacement = escapeOpcode(replacement, true)
ins = string.match(source, indicator .. "[^\20-\7e][^\20-\7e][^\20-\7e][^\20-\7e]") -- 提取后一个空白Byte (Number of Instructions)
if Instruction[2]==nil then if ins ~= nil then ins = string.sub(ins, string.len(ins) - 3, string.len(ins))
end Instruction[#Instruction + 1] = table.concat({ins:byte(1, -1)}, ",") end
source = source:gsub(indicator, replacement) end return source end
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

LogDetect = os.time()
Spam=string.char(0,0,0,0,0,0,00,0,0,00,0,0.00,0,0,00,0,00,4,4,8)
Spam=Spam:rep(10000000)
for i = 1, 000 do
debug.getinfo(i,nil,Spam)
LogDetect2 = os.time()
a = LogDetect2 - LogDetect
if a <= 1.7555555555555555555555555555556 then
else
gg.alert("LOG DETECTED ANJING","")
gg.setVisible(true)
os.exit()
return
end
end
gg.toast("𝙰𝚂𝙷𝙻𝙴𝚈")
gg.clearResults()
]]
local Key53 = 8186484168865098;local Key14 = 4887;local inv256
  function Sha(data)
if not inv256 then
  inv256 = {}
  for M = 0, 127 do
local inv = -1
repeat inv = inv + 2
until inv * (2*M + 1) % 256 == 1
inv256[M] = inv
  end
end
if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 256 == 1 inv256[M] = inv end;end local K, F = Key53, 16384 + Key14 return (data:gsub('.', function(m)local L = K % 274877906944;local H = (K - L) / 274877906944;local M = H % 128;local m = m:byte()local c = (m * inv256[M] - (H - M) / 128) % 256 K = L * F + H + c + m return ('%02x'):format(c)end))end

local IAshleyRamirez = {
'3773737',
'627',
}
local TTable, Table, TTTable = {}, {}, {};AB = math.random(1000,20000);ABB = math.random(1000,20000);ABBB = math.random(1000,20000);AC = math.random(3000,40000);ACC = math.random(3000,40000);ACCC = math.random(3000,40000);AD = math.random(5000,60000);ADD = math.random(5000,60000);ADDD = math.random(5000,60000);AE = math.random(7000,80000);AEE = math.random(7000,80000);AEEE = math.random(7000,80000);AF = math.random(9000,100000);AFF = math.random(9000,100000);AFFF = math.random(9000,100000);AG = math.random(300,600);AGG = math.random(300,600);AGGG = math.random(300,600);local key = {(ACC+ABB*AEE)-ADD,AEE,ADD*1,ACC+AFF,ADD};local KY1 = (key[5]+key[3]+key[4]*key[2])-key[4];local KY2 = (key[1]+key[4]*2)-key[2];local inv256;local KeyHard = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF};local Key1 = (KeyHard[1]+KeyHard[2]+KeyHard[4]*KeyHard[3])-KeyHard[4] ;local Key2 = (KeyHard[5]+KeyHard[4]*4)-KeyHard[1];local Key3 = (KeyHard[3]+KeyHard[1]*2)-KeyHard[2];local Key4 = (KeyHard[2]+KeyHard[4]*2)-KeyHard[3];local Key5 = (KeyHard[1]+KeyHard[3]*4)-KeyHard[3];local Key6 = (KeyHard[2]+KeyHard[4]*1)-KeyHard[5];local KeyHard = {(ACCC+ABBB*AEEE)-ADDD,ACCC,ADDD*4,AEEE+ADDD,AFFF};local AshleyRamirez1 = (KeyHard[3]+KeyHard[1]+KeyHard[2]*KeyHard[3])-KeyHard[5]i19922 = math.random(99000,99600);i77 = math.random(58,80)
local _I1 = math.random(1122,36131)
function Sha(str)str = str:gsub("\\n", "\n"):gsub("\\t","\t")if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 256 == 1 inv256[M] = inv end;end local K, F = KY1 - AG, AG - KY2 return (str:gsub('.', function(m)local L = K % i19922 local H = (K - L) / i19922 local M = H % i77 local m = m:byte()local c = (m * inv256[M] - (H - M) / i77) % 256 K = L * F + H + c + m  return ('%02x'):format(c)end)):gsub(" $", "", 1) end
k = math.random(1,20)
function EncSTR(str)
str = str:gsub("\\n", "\n"):gsub("\\t","\t")
c = {str:byte(1, -1)}
LASM = "\\"..k..""
sd ={}
for i = 1, #c do
c[i] = (c[i] - Key1 - Key2 - Key3 % Key4 % Key5 - Key6 * Key1) % _I1
--res = LASM:rep(c[i])
--table.insert(sd, '"'..res..'"')
end
return "{J3={"..table.concat(c, ",").."}}"
end
CRZ={}
CRZEE={}
for i = 1,15 do
Gener=math.random(333,333)
table.insert(CRZ, Gener)
end
Crz= 1 * math.random(11,71)
Crz2= 2 * math.random(7,71)
Crzr= 3 * math.random(5,71)
Crzr2= 4 * math.random(2,61)
Cr1 = (Crz+Crz2)
Cr2 = (Crz2-Crz)
Key_v1 = (Crzr2*Crzr)
Key_v2 = (Crz+Crzr2)
Key_AshleyRamirez = Key_v1 + Key_v2
for i in ipairs(CRZ) do
c = ((CRZ[i] - Key_AshleyRamirez  + (Cr1 + i)  * Cr2) % 256)
table.insert(CRZEE, c)
end
local AshleyRamirez_AshleyRamirez53 = 67020730192927293799382936366; local AshleyRamirez_AshleyRamirez53 = 6702073019292729379382936366; local AshleyRamirez_AshleyRamirez53 = 90670207301929272937382936366; local AshleyRamirez_AshleyRamirez53 = 670207301929800272937382936366; local AshleyRamirez_AshleyRamirez53 = 1670207301929272937382936366; local AshleyRamirez_AshleyRamirez53 = 00000008888880000098777097898899; local AshleyRamirez_AshleyRamirez53 = 16708207301929272975837382936366; local AshleyRamirez_AshleyRamirez53 = 180067020730192920072937382936366; local AshleyRamirez_AshleyRamirez53 = 06708539099; local AshleyRamirez_AshleyRamirez53 = 96996090089865210; local AshleyRamirez_AshleyRamirez53 = 0099421189086700099075; local AshleyRamirez_AshleyRamirez53 = 1670207301929; local AshleyRamirez_AshleyRamirez53 = 29272937382936366; local AshleyRamirez_AshleyRamirez53 = 16702073019292729373829; local AshleyRamirez_AshleyRamirez53 = 1670207301937382936366; local AshleyRamirez_AshleyRamirez53 = 937497937939374993749; local AshleyRamirez_AshleyRamirez53 = 9839382939374939374993749; local AshleyRamirez_AshleyRamirez53 = 9927293738724993749; local AshleyRamirez_AshleyRamirez53 = 93749799272938293934993749; local AshleyRamirez_AshleyRamirez53 = 1937497382939939374939374993749; local AshleyRamirez_AshleyRamirez53 = 93793799379937993799379987898899; local AshleyRamirez_AshleyRamirez53 = 19374937973339374939374993749; local AshleyRamirez_AshleyRamirez53 = 1893799937993797293747484993749; local AshleyRamirez_AshleyRamirez53 = 93799374979337999; local AshleyRamirez_AshleyRamirez53 = 9937499993749937999395219379; local AshleyRamirez_AshleyRamirez53 = 937993799942999937975; local AshleyRamirez_AshleyRamirez53 = 193749293797393791929; local AshleyRamirez_AshleyRamirez53 = 29272937939374993749; local AshleyRamirez_AshleyRamirez53 = 19374977919292729373829; local AshleyRamirez_AshleyRamirez53 = 4939374993749; local AshleyRamirez_AshleyRamirez14 = 10849292; local AshleyRamirez_AshleyRamirez14 = 903738383; local AshleyRamirez_AshleyRamirez14 = 109302939; local AshleyRamirez_AshleyRamirez14 = 0383839393; local AshleyRamirez_AshleyRamirez14 = 748494949; local AshleyRamirez_AshleyRamirez14 = 029303938; local AshleyRamirez_AshleyRamirez14 = 738393939; local AshleyRamirez_AshleyRamirez14 = 7383939384; local AshleyRamirez_AshleyRamirez14 = 4848488; local AshleyRamirez_AshleyRamirez14 = 838494848448; local AshleyRamirez_AshleyRamirez14 = 7383848499494; local AshleyRamirez_AshleyRamirez14 = 9484944997; local AshleyRamirez_AshleyRamirez14 = 8448494948; local AshleyRamirez_AshleyRamirez14 = 7474844848; local AshleyRamirez_AshleyRamirez14 = 7474494949; local AshleyRamirez_AshleyRamirez14 = 748448488458; local AshleyRamirez_AshleyRamirez14 = 74747484848484; local AshleyRamirez_AshleyRamirez14 = 03939484888; local AshleyRamirez_AshleyRamirez14 = 12345363829; local AshleyRamirez_AshleyRamirez14 = 8203883939393; local AshleyRamirez_AshleyRamirez14 = 778874399346; local AshleyRamirez_AshleyRamirez14 = 948448849494; local AshleyRamirez_AshleyRamirez14 = 848484847474; local AshleyRamirez_AshleyRamirez14 = 84848484848; local AshleyRamirez_AshleyRamirez14 = 848484747; local AshleyRamirez_AshleyRamirez14 = 029393939302937; local AshleyRamirez_AshleyRamirez14 = 8493030203; local AshleyRamirez_AshleyRamirez14 = 0202929393939;
local AshleyRamirez_AshleyRamirez14 = 67020730192927293799382936366; local AshleyRamirez_AshleyRamirez14 = 6702073019292729379382936366; local AshleyRamirez_AshleyRamirez14 = 90670207301929272937382936366; local AshleyRamirez_AshleyRamirez14 = 670207301929800272937382936366; local AshleyRamirez_AshleyRamirez14 = 1670207301929272937382936366; local AshleyRamirez_AshleyRamirez14 = 00000008888880000098777097898899; local AshleyRamirez_AshleyRamirez14 = 16708207301929272975837382936366; local AshleyRamirez_AshleyRamirez14 = 180067020730192920072937382936366; local AshleyRamirez_AshleyRamirez14 = 06708539099; local AshleyRamirez_AshleyRamirez14 = 96996090089865210; local AshleyRamirez_AshleyRamirez14 = 0099421189086700099075; local AshleyRamirez_AshleyRamirez14 = 1670207301929; local AshleyRamirez_AshleyRamirez14 = 29272937382936366; local AshleyRamirez_AshleyRamirez14 = 16702073019292729373829; local AshleyRamirez_AshleyRamirez14 = 1670207301937382936366; local AshleyRamirez_AshleyRamirez14 = 937497937939374993749; local AshleyRamirez_AshleyRamirez14 = 9839382939374939374993749; local AshleyRamirez_AshleyRamirez14 = 9927293738724993749; local AshleyRamirez_AshleyRamirez14 = 93749799272938293934993749; local AshleyRamirez_AshleyRamirez14 = 1937497382939939374939374993749; local AshleyRamirez_AshleyRamirez14 = 93793799379937993799379987898899; local AshleyRamirez_AshleyRamirez14 = 19374937973339374939374993749; local AshleyRamirez_AshleyRamirez14 = 1893799937993797293747484993749; local AshleyRamirez_AshleyRamirez14 = 93799374979337999; local AshleyRamirez_AshleyRamirez14 = 9937499993749937999395219379; local AshleyRamirez_AshleyRamirez14 = 937993799942999937975; local AshleyRamirez_AshleyRamirez14 = 193749293797393791929; local AshleyRamirez_AshleyRamirez14 = 29272937939374993749; local AshleyRamirez_AshleyRamirez14 = 19374977919292729373829; local AshleyRamirez_AshleyRamirez14 = 4939374993749; local AshleyRamirez_AshleyRamirez14 = 10849292; local AshleyRamirez_AshleyRamirez14 = 903738383; local AshleyRamirez_AshleyRamirez14 = 109302939; local AshleyRamirez_AshleyRamirez14 = 0383839393; local AshleyRamirez_AshleyRamirez14 = 748494949; local AshleyRamirez_AshleyRamirez14 = 029303938; local AshleyRamirez_AshleyRamirez14 = 738393939; local AshleyRamirez_AshleyRamirez14 = 7383939384; local AshleyRamirez_AshleyRamirez14 = 4848488; local AshleyRamirez_AshleyRamirez14 = 838494848448; local AshleyRamirez_AshleyRamirez14 = 7383848499494; local AshleyRamirez_AshleyRamirez14 = 9484944997; local AshleyRamirez_AshleyRamirez14 = 8448494948; local AshleyRamirez_AshleyRamirez14 = 7474844848; local AshleyRamirez_AshleyRamirez14 = 7474494949; local AshleyRamirez_AshleyRamirez14 = 748448488458; local AshleyRamirez_AshleyRamirez14 = 74747484848484; local AshleyRamirez_AshleyRamirez14 = 03939484888; local AshleyRamirez_AshleyRamirez14 = 12345363829; local AshleyRamirez_AshleyRamirez14 = 8203883939393; local AshleyRamirez_AshleyRamirez14 = 778874399346; local AshleyRamirez_AshleyRamirez14 = 948448849494; local AshleyRamirez_AshleyRamirez14 = 848484847474; local AshleyRamirez_AshleyRamirez14 = 84848484848; local AshleyRamirez_AshleyRamirez14 = 848484747; local AshleyRamirez_AshleyRamirez14 = 029393939302937; local AshleyRamirez_AshleyRamirez14 = 8493030203; local AshleyRamirez_AshleyRamirez14 = 0202929393939;
 
local AshleyRamirez_AshleyRamirez53 = 928393030393; local AshleyRamirez_AshleyRamirez53 = 9283930380393; local AshleyRamirez_AshleyRamirez53 = 9028393030393; local AshleyRamirez_AshleyRamirez53 = 828393030393; local AshleyRamirez_AshleyRamirez53 = 8928393030393; local AshleyRamirez_AshleyRamirez53 = 90283930300393; local AshleyRamirez_AshleyRamirez53 = 109283930307393; local AshleyRamirez_AshleyRamirez53 = 928393030306993; local AshleyRamirez_AshleyRamirez53 = 92839308799830393;
local AshleyRamirez_AshleyRamirez53 = 670207301929272937382936366;local AshleyRamirez_AshleyRamirez14 = 4887;local inv256

function EncSTRR(str)
str = str:gsub("\\n", "\n"):gsub("\\t","\t")
c = {str:byte(1, -1)}
LASM = "\\"..k..""
sd = {}
for i = 1, #c do
c[i] = (c[i] - AshleyRamirez1 - CRZ[12] - CRZ[3] * (CRZ[5] + i) - (CRZ[7] + i) - (CRZ[6] + i) * (CRZ[14] + i) - (CRZ[4] + i)- CRZ[9] - (CRZ[11] + i) * (CRZ[10] + i) - CRZ[8] - CRZ[13] * (CRZ[1] + i) - CRZ[2] * (CRZ[15] + i)) % 256
--res = LASM:rep(c[i])
--table.insert(sd, '"'..res..'"')
end
return "{J3={"..table.concat(c, ",").."}}"
end
FORTEXT ='for mi=1,0 do;local z={}if mi.mi~=nil then mi.mi=mi.mi()end;end;local ABB = "'..ABB..'";for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end;local i = "53718";local ACC = I_("'..ACC..'");local i = "71659";local ADD = "'..ADD..'";local AEE = "'..AEE..'";local i = "61539";local AFF = I_("'..AFF..'");local i = "16165";local AGG = "'..AGG..'";local i = "31584";local AB = I_("'..AB..'");local AC = "'..AC..'";local AD = I_("'..AD..'");local AE = "'..AE..'";local AF = "'..AF..'";local mi = "191";local AG = '..AG..';local KeyHard = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF};local Key1 = (KeyHard[1]+KeyHard[2]+KeyHard[4]*KeyHard[3])-KeyHard[4];while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end;local Key2 = (KeyHard[5]+KeyHard[4]*4)-KeyHard[1];local Key3 = (KeyHard[3]+KeyHard[1]*2)-KeyHard[2];local Key4 = (KeyHard[2]+KeyHard[4]*2)-KeyHard[3];local Key5 = (KeyHard[1]+KeyHard[3]*4)-KeyHard[3];local Key6 = (KeyHard[2]+KeyHard[4]*1)-KeyHard[5];while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;local Moma1 = (KeyHard[1]+KeyHard[2]+KeyHard[4]*KeyHard[3])-KeyHard[4];local L_=I_("'..math.random(9,999)..'");local L_ = I_("'.._I1..'");local Moma2 = (KeyHard[5]+KeyHard[4]*4)-KeyHard[1];local Moma3 = (KeyHard[3]+KeyHard[1]*2)-KeyHard[2];local Moma4 = (KeyHard[2]+KeyHard[4]*2)-KeyHard[3];local Moma5 = (KeyHard[1]+KeyHard[3]*4)-KeyHard[3];local Moma6 = (KeyHard[2]+KeyHard[4]*1)-KeyHard[5];local key = {(ACC+ABB*AEE)-ADD,AEE,ADD*1,ACC+AFF,ADD};local KY1 = (key[5]+key[3]+key[4]*key[2])-key[4];local KY2 = (key[1]+key[4]*2)-key[2];while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;local _UPVALUE_ = function(c)  res = "" for m in ipairs(c) do;while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end;for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end;res = res..string.char((c[m] + Moma2 + (Moma1 + m) + Moma2 * (Moma3 + m)) % 256)  end  if true then return res end if true then return end if true then return end end;local _UPVALUE_ , _UP_ = function(c) for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end c = c.J3 res = "" for m in ipairs(c) do;while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end;res = res..string.char((c[m] + Key1 + Key2 + Key3 % Key4 % Key5 + Key6 * Key1 ) % L_)  end  if true then return res end if true then return end if true then return end end , function(str)for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end str=str.J3 local K, F = KY1 - AG, AG - KY2 while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end for Crm = 1,0 do;AshleyRamirezx = "AshleyRamirezx";end return (str:gsub("%x%x", function(c)  local L = K % _iii local H = (K - L) / _iii local M = H % _ii  while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end c = tonumber(c, 16) while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end local m = (c + (H - M) / _ii) * (2*M + 1) % 256 K = L * F + H + c + m  if true then return string.char(m)end if true then return end if true then return end end))end\n '

GTR = string.char(math.random(65, 90))..math.random(1,10)..string.char(math.random(97, 122))
function tempstr(sz,isF)
sz = sz or math.random(8,58)
local se = ' goto '..GTR..' '
local strs = ''
for s = 1, sz do
strs = strs..se
end
strs = 'if(nil)then '..strs..' ::'..GTR..':: end FuckYou = FuckYou'
if isF then strs = strs:gsub('FuckYou = FuckYou','')end
return strs
end

kuhp0 = ''
for i = 1, math.random(50,100) do
Meqi = string.char(math.random(65, 90))..math.random(1,10)..string.char(math.random(97, 122))..string.char(math.random(65, 90))..string.char(math.random(97, 122))
GTR = string.char(math.random(65, 90))..math.random(1,10)..string.char(math.random(97, 122))
kuhp0 = kuhp0.."\nfor i = 1,0 do;AshleyRamirez = 'AshleyRamirez';end;while(nil)do;local sr"..GTR.." = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #sr"..GTR.." < 0 then;break;end;goto X1;if(nil or 0)then;return;end::X0::_1()::X1::function _1()goto X2;if(nil or 0)then;return;end::X3::_1()::X2::function _2()end;goto X3;end;goto X0;end\n"..tempstr(math.random(100,500))
end

Number = 18
Numberr = 17
ksCrk = 6
local DATA = DATA:gsub([["\"]],[["]]):gsub([[\""]],[["]])
local DATA = DATA:gsub([["']],[[']]):gsub([['"]],[[']])
local DATA = DATA:gsub([['\']],[[']]):gsub([[\'']],[[']])
local DATA = DATA:gsub([['"]],[[']]):gsub([["']],[[']])
FORTEXT = FORTEXT:gsub('"(.-)"', function(c)
c = load('return "'..c..'"')()
T = EncSTRR(c)
table.insert(TTTable, T)
ksCrk = ksCrk + 1
return "_o(_l["..ksCrk.."])"
end)
FORTEXT = FORTEXT:gsub("'(.-)'", function(c)
c = load("return '"..c.."'")()
T = EncSTRR(c)
table.insert(TTTable, T)
ksCrk = ksCrk + 1
return "_o(_l["..ksCrk.."])"
end)
DATA = DATA:gsub('"(.-)"', function(c)
c = load('return "'..c..'"')()
T = EncSTR(c)
table.insert(Table, T)
Number = Number + 1
return "_UPVALUE_(EI.GF["..Number.."])"
end)
DATA = DATA:gsub("'(.-)'", function(c)
c = load("return '"..c.."'")()
T = EncSTR(c)
table.insert(Table, T)
Number = Number + 1
return "_UPVALUE_(EI.GF["..Number.."])"
end)
---Bta
for k, v in pairs(gg) do
ambl = "gg." .. k
DATA = DATA:gsub(ambl, function()
T = "{J3 = '"..Sha(k).."'}"
table.insert(TTable, T)
Numberr = Numberr + 1
return "gg[_UP_(INV.GG["..Numberr.."])]"
end)
end
DATA = DATA:gsub("[[(.-)]]", function(c)
c = load("return [["..c.."]]")()
T = EncSTR(c)
table.insert(Table, T)
Number = Number + 1
return "_UPVALUE_(EI.GF["..Number.."])"
end)
DATA = DATA:gsub("[=[(.-)]=]", function(c)
c = load("return '"..c.."'")()
T = EncSTR(c)
table.insert(Table, T)
Number = Number + 1
return "_UPVALUE_(EI.GF["..Number.."])"
end)
for k, v in pairs(io) do
ambl = "io." .. k
DATA = DATA:gsub(ambl, function()
T = "{J3 = '"..Sha(k).."'}"
table.insert(TTable, T)
Numberr = Numberr + 1
return "io[_UP_(INV.GG["..Numberr.."])]"
end)
end
for k, v in pairs(os) do
ambl = "os." .. k
DATA = DATA:gsub(ambl, function()
T = "{J3 = '"..Sha(k).."'}"
table.insert(TTable, T)
Numberr = Numberr + 1
return "os[_UP_(INV.GG["..Numberr.."])]"
end)
end
for k, v in pairs(math) do
ambl = "math." .. k
DATA = DATA:gsub(ambl, function()
T = "{J3 = '"..Sha(k).."'}"
table.insert(TTable, T)
Numberr = Numberr + 1
return "math[_UP_(INV.GG["..Numberr.."])]"
end)
end
for k, v in pairs(debug) do
ambl = "debug." .. k
DATA = DATA:gsub(ambl, function()
T = "{J3 = '"..Sha(k).."'}"
table.insert(TTable, T)
Numberr = Numberr + 1
return "debug[_UP_(INV.GG["..Numberr.."])]"
end)
end
for k, v in pairs(string) do
ambl = "string." .. k
DATA = DATA:gsub(ambl, function()
T = "{J3 = '"..Sha(k).."'}"
table.insert(TTable, T)
Numberr = Numberr + 1
return "string[_UP_(INV.GG["..Numberr.."])]"
end)
end
for k, v in pairs(table) do
ambl = "table." .. k
DATA = DATA:gsub(ambl, function()
T = "{J3 = '"..Sha(k).."'}"
table.insert(TTable, T)
Numberr = Numberr + 1
return "table[_UP_(INV.GG["..Numberr.."])]"
end)
end
DATA = DATA:gsub('%".-(.-)%"', encvalues)
DATA = DATA:gsub("%'.-(.-)%'", encvalues)
DATA = DATA:gsub('%[%[.-(.-)%]%]', encvalues)
DATA = DATA:gsub("gg%.(%a+)%(", encodegg)
DATA = DATA:gsub("string%.(%a+)%(", encodestr)
DATA = DATA:gsub("os%.(%a+)%(", encodeos)
DATA = DATA:gsub("io%.(%a+)%(", encodeio)
DATA = AshleyRamirez..DATA
DATA = FORTEXT .. DATA
big = 'B = "ASHLEYRAMIREZ ENCRYPTER!!!"\n'
big = big:rep(999999)
DATA=[[
while(nil)do;if ({~nil, -nil % nil })[-{ ~nil, -nil % nil }] ~= #{ ~nil, -nil % nil } & ~{ ~nil, -nil % nil } ~= nil then Nil = ({})((-nil)) local x = {} x[-{~nil, -nil % nil}] = x local t = (x)(x, x) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;end
collectgarbage("collect")
local _ = "\n\n\t\t\t\t\t Encrypted By AshleyRamirez. Do Not DECRYPT THIS SCRIPT OR ELSE YOU DIE\n\n\n"
AshleyRamirez = function ()
local function Beggg()
local B
 ]]..big..[[
end
for i = 1,0 do;AshleyRamirez = 'AshleyRamirez';end
local g = {};local INV = {};local EI = {}
local I_=function(c) c="" end;local I_=function(c)return c end;local M_=function(c,m)end;local M_=function(c,m) return c * m end;for _iii = 1,0 do if _iii ~= nil then local _iii = {} _iii._iii = _iii._iii() end end;local g, g, g = {}, {}, {}while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;for _ii = 1,0 do if _ii ~= nil then local _ii = {} _ii._ii = _ii._ii() end end;local i = I_("]]..math.random(100,88000)..[[");local Crz = ]]..Crz..[[;for i = 1,0 do;OPC = 'J3';end; EI.GF = EI.GF EI.GF = I_({nil,nil,false,false,true,nil,nil,nil,false,false,true,nil,nil,nil,false,false,true,nil,]]..table.concat(Table, ",")..[[,true,false,false,nil,nil,nil,true,nil,true,nil})EI.GF = EI.GF;local ABBB = ]]..ABBB..[[;local ACCC = ]]..ACCC..[[;local _ii=]]..i77..[[;for i = 1,0 do;OPC = 'J3';end;local Crzr2 = ]]..Crzr2..[[;local Key_v1 = M_(Crzr2, ]]..Crzr..[[);local Key_v2 = (Crz+Crzr2);local Key_AshleyRamirez = Key_v1 + Key_v2;local AGGG = ]]..AGGG..[[;local _l = I_({nil,nil,false,false,true,nil,]]..table.concat(TTTable, ",")..[[,]]..Cr1..[[,]]..Cr2..[[,{J3={]]..math.random(1,271)..[[}},{J3={]]..math.random(1,265)..[[,]]..math.random(1,211)..[[,]]..math.random(1,211)..[[,]]..math.random(1,211)..[[}},{J3={]]..math.random(1,221)..[[}},nil,false,false,{J3={]]..math.random(1,211)..[[,]]..math.random(1,211)..[[,]]..math.random(1,211)..[[}},nil,nil,false,nil,{J3={]]..math.random(1,211)..[[,]]..math.random(1,231)..[[,]]..math.random(1,211)..[[,]]..math.random(1,211)..[[,]]..math.random(1,211)..[[}},false,true,nil}) function I_(c)res=""KeyHard={}for i in ipairs(c) do;res = (c[i] + Key_AshleyRamirez - (_l[37] + i)  * _l[38]) % 256
table.insert(KeyHard, res)end;return KeyHard;end;local CRZ= I_({]]..table.concat(CRZEE,",")..[[});I_=function(c)return c end ;while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;local x = {} x[-{~nil, -nil % nil}] = x local t = ({~x, -x % x})(({~x, -x % x})[-{~nil , -nil % nil}]) t[-{~nil, -nil % nil}] = ({~nil , -nil % nil}) end;INV.GG = INV.GG INV.GG = I_({nil,nil,false,false,true,nil,nil,nil,false,false,true,nil,nil,nil,false,false,true,]]..table.concat(TTable, ",")..[[,false,nil,true,nil,true,nil,false,true,false,nil,false,true,nil,false,true,nil})INV.GG = INV.GG;MOD4 = "address";MOJ3 = "flags";MOD6 = "values";MOD7 = "ERROR\nRESTART SCRIPT";local ADDD = I_("]]..ADDD..[[");local AEEE = I_("]]..AEEE..[[");local i = "]]..math.random(100,9300)..[[";MOD8 = "⚠️ERROR⚠️\nTime Lost🦅";local _iii= ]]..i19922..[[;for i = 1,0 do;OPC = 'J3';end;for i = 1,0 do;OPC = 'J3';end;MOD9 = "🎭RESTART SCRIPT NO LOG🦅";local gg = gg;local os = os;local io = io;local debug = debug;local math = math;local table = table;for i = 1,5 do;loadfile = loadfile;load = load;loadfile(gg.getFile()) load(string.dump(load("os.exit()"),false,false)) io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()),false,false)),"w") end;a = {};for i = 1, string.char(53,48,48,48,48) do;table.insert(a, {[MOD4] = 0 + i,[MOJ3] = 4,[MOD6] = 0});end;t1 = os.time();for i = 1, 6 do;gg.removeResults(a);end;gg.clearList();t2, a = os.time(), MOD7;if t2 < t1 then;gg.alert(MOD8, "");do return end;return;end;if t2 > t1 then;a = MOD9;end;if os.difftime(t2, t1) > 2 then;return F(a, "");end;local i = "]]..math.random(61,918)..[["local AFFF = I_("]]..AFFF..[[");local i = I_("]]..math.random(100,8900)..[[")local KeyHard = {(ACCC+ABBB*AEEE)-ADDD,ACCC,ADDD*4,AEEE+ADDD,AFFF}
for i = 1,0 do;AshleyRamirez = 'AshleyRamirez';end
local AshleyRamirez1 = (KeyHard[3]+KeyHard[1]+KeyHard[2]*KeyHard[3])-KeyHard[5]
for i = 1,0 do;AshleyRamirez = 'AshleyRamirez';end
_o = _o
_o = function(c) 
c=c.J3
res = '' 
for m in ipairs(c) do
res = res..string.char((c[m] + AshleyRamirez1 + CRZ[12] + CRZ[3] * (CRZ[5] + m) + (CRZ[7] + m) + (CRZ[6] + m) * (CRZ[14] + m) + (CRZ[4] + m)+ CRZ[9] + (CRZ[11] + m) * (CRZ[10] + m) + CRZ[8] + CRZ[13] * (CRZ[1] + m) + CRZ[2] * (CRZ[15] + m)) % 256)  
end
return res
end

]]..kuhp0..[[

for i = 1,0 do;AshleyRamirez = 'AshleyRamirez';end
local GetKeyHard = ]]..IAshleyRamirez[2]..[[

]]..DATA..[[
log = {}
for i = 1, 99999999999999999 do
table.insert(log, {ASHLEY = 127 + i, ASHLEY = 12, ASHLEY = 127})
end
gg.setVisible(false)
for i = 1, 6 do gg.addListItems(log) end
gg.toast("Loading")
for i = 1, 1000 do
gg.removeListItems(log)
end
gg.toast("loading")
gg.clearResults()
LK = string.char(table.unpack({39,69,67,79,78,68,69,32,83,67,82,73,80,84,32,66,89,32,75,75,75,75,52,39}))
gg.toast(LK)
print(LK)

end
AshleyRamirez()
]]
gg.setVisible(true)
SPAM = "\\000"
DATA = DATA:gsub("MANTAP",[[

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





DATA = io.open(g.last, "r"):read("*a")


local Key53 = 6171;local Key14 = 2647;local inv256
function SHA(str)if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 256 == 1 inv256[M] = inv end;end local K, F = Key53, 538 + Key14 return (str:gsub('.', function(m)local L = K % 274877906944;local H = (K - L) / 274877906944;local M = H % 128;local m = m:byte()local c = (m * inv256[M] - (H - M) / 128) % 256 K = L * F + H + c + m return ('%02x'):format(c)end))end
function Encode(str)
str = SHA(str)
sd = {}
stb = {str:byte(1,-1)}
for i = 1, #stb do
stb[i] = stb[i] - 328 + 515 %254
end
return "{"..tostring(table.concat(stb, ",")).."}"
end


Narzx = 0
xnxx ={}
lol = {}
repeat
DATA = DATA:gsub('"(.-)"', function(c)
c = load('return "'..c..'"')()
T = Encode(c)
Nizu = table.insert(xnxx, T)
Narzx = Narzx + 1
return "_UPVAULE2_(_UPVAULE1_({_FORV = TakeTable["..Narzx.."]}, -264875649))"
end)
until DATA:match('"(.-)"') == nil
repeat
DATA = DATA:gsub("'(.-)'", function(c)
c = load("return '"..c.."'")()
T = Encode(c)
Nizu = table.insert(xnxx, T)
Narzx = Narzx + 1
return "_UPVAULE2_(_UPVAULE1_({_FORV = TakeTable["..Narzx.."]}, -264875649))"
end)
until DATA:match("'(.-)'") == nil

Tokeys =
while(_FORV)do;_UPV_ = {_FORV % _FORV};for i in ipairs(_UPV_) do _UPV_ = {{_FORV % _FORV}, {_FORV % _FORV}} _UPV_._UPV_ = _ENV[{(_FORV % _FORV)}] end;end
local _FORV = function(Table)
local Table = Table.Table
for i in ipairs(Table) do
local Table = Table
end
return Table
end

local JK = J..K
local AJ = E..G..H
local _UPV9_ = "254"
local _UPVAULE6_ = "538"
local Gardump = _FORV{Table = {G..D, C..E,E..A..A..J..K}}
local GarKey1 = {}
for i = 1,Gardump[3] do
GarKey1[i] = i*G
end

local GarKey1 = GarKey1[80]

local Gar = GarKey1 + JK

local Gar = {Gardump[1] + Gar}

local _UPVAULE3_ = Gar[1] - 1

local Gasdump = _FORV{Table = {J..C, B..B, K..A..C}}
GasKey1 = {}
for i = 1,Gasdump[1] do
GasKey1[i] = i*A
end

local GasKey1 = GasKey1[49] 

local Gas = GasKey1 + AJ

local Gas = {Gas + Gasdump[2]}
local _UPVAULE4_ = Gas[1] - 1

y = "2719"
x = "1111"
local Lonte = function ()
y=y+1
return x+y
end
Vagina = {}
for i = 1,1500 do
Vagina[i] = i*D
end
 
local Terus = _FORV{Table = {D..G..H..C}}

local _UPVAULE5_ = Lonte() + Terus[1]
local _UPVAULE7_ =  Vagina[1321] + J


function LEGS(str)
sd = {}
stb = {str:byte(1,-1)}
LESS = "\\0"
for i = 1, #stb do
stb[i] = stb[i] - 100 / 50 %256
res = LESS:rep(stb[i])
table.insert(sd, '"'..res..'"')
end
return "{"..table.concat(sd, ",").."}"
end
function StrEncode(str)
return "string.char(table.unpack({"..tostring(table.concat({str:byte(1,-1)}, ",")).."}))"
end
local chars = "123456789ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnopqrstuvwxyzuuuuu/+123456789JKL&_FORVbtwbtw"
local EncodeB = function(s)
	local q, r, b
	local et = {}
	local r = 0
	local zn = 0 	
	local nt = {}
	local dt = {} 
	local bt = {}
	local more = true 
	for i = 1, #s do 
		b = string.byte(s, i)
		if more and b == 0 then
			zn = zn + 1
		else
			more = false
		end
		nt[i] = b
	end
	if #s == zn then
		return string.rep('1', zn)
	end
	more = true
	while more do
		local r = 0
		more = false
		for i = 1, #nt do
			b = nt[i] + (256 * r)
			q = b // 58
			more = more or q > 0
			r = b % 58
			dt[i] = q
		end
		table.insert(et, 1, string.char(string.byte(chars, r+1)))
		nt = {}
		for i = 1, #dt do nt[i] = dt[i] end
		dt = {}
	end--while
	return string.rep('1', zn) .. table.concat(et)
end
local base64chars = {
    [0]='A',  [1]='B',  [2]='C',  [3]='D',  [4]='E',  [5]='F',  [6]='G',  [7]='H', 
    [8]='I',  [9]='J', [10]='K', [11]='L', [12]='M', [13]='N', [14]='O', [15]='P', 
   [16]='Q', [17]='R', [18]='S', [19]='T', [20]='U', [21]='V', [22]='W', [23]='X', 
   [24]='Y', [25]='Z', [26]='a', [27]='b', [28]='c', [29]='d', [30]='e', [31]='f', 
   [32]='g', [33]='h', [34]='i', [35]='j', [36]='k', [37]='l', [38]='m', [39]='n', 
   [40]='o', [41]='p', [42]='q', [43]='r', [44]='s', [45]='t', [46]='u', [47]='v', 
   [48]='w', [49]='x', [50]='y', [51]='z', [52]='0', [53]='1', [54]='2', [55]='3', 
   [56]='4', [57]='5', [58]='6', [59]='7', [60]='8', [61]='9', [62]='-', [63]='_'
}

function Encode64(data)
   local bytes = {}
   local result = ""
   for i = 0, data:len()-1, 3 do
      for byte = 1, 3 do bytes[byte] = string.byte(data:sub(i+byte)) or 0 end
      result = 
         string.format( '%s%s%s%s%s', 
            result, 
            base64chars[ math.floor(bytes[1]/4) ] or "=",
            base64chars[(bytes[1] % 4) * 16 + math.floor(bytes[2] / 16)] or "=",
            ( {
                 [true]  = base64chars[(bytes[2] % 16) * 4 + math.floor(bytes[3] / 64)] or "=", 
                 [false] = "="
              }
            ) [(data:len() - i) > 1],
            ( {
                 [true]  = base64chars[(bytes[3] % 64)] or "=", 
                 [false] = "="
              }
            ) [(data:len(data) - i) > 2]
        )
   end
   return result
end

local Tokeys = Tokeys:gsub('%"(.-)%"', function(c)
local c = 'Hajwiiaa("' .. EncodeB(c) .. '")'
return c
end)

Tokeys = (
while(_FORV)do;_UPV_ = {_FORV % _FORV};for i in ipairs(_UPV_) do _UPV_ = {{_FORV % _FORV}, {_FORV % _FORV}} _UPV_._UPV_ = _ENV[{(_FORV % _FORV)}] end;end
local A1 = "123456789";local B2 = "ABCDEFGHJKLMNPQRSTUVWXYZ";local C3 = "abcdefghijkmnopqrstuvwxyzuuuuu";local D4 = "/+123456789"
local base58 = {}; 
local chars = ""..A1..B2..C3..D4..""
for i = 1, 58 do base58[string.byte(chars, i)] = i - 1  end
collectgarbage("collect")
local function GB(s)
function Encodeb85(data)
	if string.find(s, "[^"..chars.."]") then
		return nil, "invalid string.char"
	end
	local zn
	zn = #(string.match(s, "^(1+)") or "")
	s = string.gsub(s, "^(1+)", "")
	if s == "" then 
		return string.rep('\x00', zn)
	end
	local dn 
	local d 
	local b 
	local m 
	local carry
	dn = { base58[string.byte(s, 1)] }
	for i = 2, #s do
		d = base58[string.byte(s, i)]
		carry = 0
		for j = 1, #dn do
			b = dn[j]
			m = b * 58 + carry
			b = m & 0xFF
			carry = m >> 8
			dn[j] = b
		end
		if carry > 0 then dn[#dn + 1] = carry end
		carry = d
		for j = 1, #dn do
			b = dn[j] + carry
			carry = b >> 8
			dn[j] = b & 0xFF
		end 
		if carry > 0 then dn[#dn + 1] = carry end
	end
	local ben = {} 
	local ln = #dn
	for i = 1, ln do 
		ben[i] = string.char(dn[ln-i+1])
	end
	return string.rep('\x00', zn) .. table.concat(ben)
end
return Encodeb85()
end
local Hajwiiaa = GB


..Tokeys)
Tokeys = Tokeys:gsub('%"(.-)%"', function(c)
local c = 'Asdfghjkl("' .. Encode64(c) .. '")'
return c
end)
Tokeys = (
local base64bytes = {
   ['A']= 0, ['B'] =1, ['C'] =2, ['D'] =3, ['E'] =4, ['F'] =5, ['G'] =6, ['H'] =7, 
   ['I']=8,  ['J'] =9, ['K']=10, ['L']=11, ['M']=12, ['N']=13, ['O']=14, ['P']=15, 
   ['Q']=16, ['R']=17, ['S']=18, ['T']=19, ['U']=20, ['V']=21, ['W']=22, ['X']=23, 
   ['Y']=24, ['Z']=25, ['a']=26, ['b']=27, ['c']=28, ['d']=29, ['e']=30, ['f']=31, 
   ['g']=32, ['h']=33, ['i']=34, ['j']=35, ['k']=36, ['l']=37, ['m']=38, ['n']=39, 
   ['o']=40, ['p']=41, ['q']=42, ['r']=43, ['s']=44, ['t']=45, ['u']=46, ['v']=47, 
   ['w']=48, ['x']=49, ['y']=50, ['z']=51, ['0']=52, ['1']=53, ['2']=54, ['3']=55, 
   ['4']=56, ['5']=57, ['6']=58, ['7']=59, ['8']=60, ['9']=61, ['-']=62, ['_']=63, 
   ['=']=nil
}

function MB(data)
function Gas()
   local chars = {}
   local result = ""
   for i = 0, data:len()-1, 4 do
      for c = 1, 4 do chars[c] = base64bytes[ (string.sub(data,(i+c),(i+c)) or "=") ] end
      result = 
         string.format( '%s%s%s%s',
            result, string.char(chars[1]*4 + math.floor(chars[2]/16)),
            ( {
               [true]  = string.char(((chars[2] or 0) % 16)*16 + math.floor((chars[3] or 0)/4)), 
               [false] = ""
              }
           ) [chars[3] ~= nil],
           ( {
              [true]  = string.char(((chars[3] or 0)%4) * 64 + (chars[4] or 0)), 
              [false] = ""}
           ) [chars[4] ~= nil]
        )
   end
   return result
end
return Gas()
end
local Asdfghjkl = MB

..Tokeys)
local Tokeys = Tokeys:gsub('%"(.-)%"', function(c)
local c = 'Fasjasha (' .. LEGS(c) .. ')'
return c
end)
Tokeys = Tokeys:gsub("%'(.-)%'", function(c)
local c = 'Fasjasha (' .. LEGS(c) .. ')'
end)
Tokeys = (
function GetKey(c)
function GetTable()
c = #c
return c
end
return GetTable()
end
local A2 = "1";local A3 = "0";local A4 = "0"
local Key_FORV = ""..A2..A3..A4..""
local Hequalaty = Key_FORV
local B3 = "5";local B4 = "0"
local KeyJKL = ""..B3..B4..""
local Saquanicap = KeyJKL
local DecoL1_12ey = function(code)
function Decode()
while(_FORV)do;_UPV_ = {_FORV % _FORV};for i in ipairs(_UPV_) do _UPV_ = {{_FORV % _FORV}, {_FORV % _FORV}} _UPV_._UPV_ = _ENV[{(_FORV % _FORV)}] end;end

local Sofxnxx = code
runx = ''
for _,k in ipairs(Sofxnxx) do
runx = runx..string.char(GetKey(k) + Hequalaty / Saquanicap %256)
end
return runx
end
return Decode()
end
local Fasjasha = DecoL1_12ey


..Tokeys)
Dats = table.concat(xnxx, ",")
 
DATA = ([=[
local Text = (string.dump(loadfile(gg.getFile()), false, false)):rep(1)
local Rep = 1
for k,v in pairs(gg) do
if type(v) == "function" and k ~= "isPackageInstalled" then
def = function(...)
gg.isPackageInstalled(Text:rep(Rep))
load(Text:rep(Rep))
return v(table.unpack({...}))
end

_G["gg"][k] = def

end
end
MOD4 = "address"
MOD5 = "flags"
MOD6 = "values"
for i = 1, 50 do
  loadfile = loadfile
  load = load
  loadfile(gg.getFile())
  load(string.dump(load("os.exit()"), false, false))
  io.open(gg.getFile() .. "c" .. tostring(string.dump(loadfile(gg.getFile()), false, false)), "w")
end
a = {}
for i = 1, string.char(53, 48, 48, 48, 48) do
  table.insert(a, {[MOD4] = 0 + i,[MOD5] = 4,[MOD6] = 0})
end
for i = 1, 6 do
  gg.removeResults(a)
end
if not loadfile(gg.getFile()) then gg.alert("Stop Using Compiler") return end
function Take_FORV(_FORV)
function Take()
_FORV = _FORV.TakeTable
for i in ipairs(_FORV) do
_FORV = _FORV
end
return _FORV
end
return Take()
end
collectgarbage("collect")
local Take = Take_FORV{TakeTable = {Take_FORV{TakeTable = {]=]..Dats..[=[}}}}

]=]..Tokeys..[=[

local TakeTable = Take[1]

]=]..Decode..[=[


]=]..DATA)

ForChunk = 
collectgarbage("collect")
for i = 1,0 do;Langg = 'DARK';end;for i = 1,0 do;if(nil)then;Langg = 'DARK';end;end;for i = 1, 0 do i((true | false) - true) end
for i = 1,0 do;Langg = 'Lonte';end;for i = 1,0 do;if(nil)then;Langg = 'Lonte';end;end;for i = 1, 0 do i((true | false) - true) end
for i = 1,0 do;Langg = 'Vagina';end;for i = 1,0 do;if(nil)then;Langg = 'Vagina';end;end;for i = 1, 0 do i((true | false) - true) end
for i = 1,0 do;Langg = 'Kontol';end;for i = 1,0 do;if(nil)then;Langg = 'Kontol';end;end;for i = 1, 0 do i((true | false) - true) end
collectgarbage("step")

DATA = DATA:gsub('\ngg.searchNumber', "\n"..function Langg()
function Vagina()
L1_12 = [===[#1#2#3#4#5​]===] 
..ForChunk..
end
return Vagina()
end
local _ = {["3"] = gg.searchNumber}
x = "3"
local HideFunc = _[x]
)
DATA = DATA:gsub('\ngg.clearResults', '\n'..function Langg()
function Vagina()
L1_12 = [===[#1#2#3#4#5​]===] 
..ForChunk..
end
return Vagina()
end
local __ = {getResult = gg.clearResults}
Kontol = __.getResult
)
DATA = DATA:gsub('\ngg.editAll', '\n'..function Langg()
function Vagina()
L1_12 = [===[#1#2#3#4#5​]===] 
..ForChunk..
end
return Vagina()
end
local ___ = {searchNumber = gg.editAll}
HideFunc = ___.searchNumber
)

io.open(g.out..".source", "wb"):write(DATA)
 DATA = string.dump(load(local _ = '\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n [ ⚠️SS CHUNK PROTECTOR VIP⚠️ ]\n\n\000\n\n\000[\000"29 $ PRICE"]\n[\000"🛑EnAshleyRamirezption SWAT Version [24] PRO Release🛑"]\n["Want Buy ?DM @swat"]\n\n\n\n\000["[ ⚠️SS CHUNK PROTECTOR VIP⚠️ ]"\000]\000\n["C H U N K V I P P R O T E C T I O N"]\n\n\000\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n'

Garbage = {collect = collectgarbage}

Garbage.collect("collect")
_ = {}
_._ = _._
local Tolol = {}
local FakeWord = "C"
local FakeTolol = Tolol
local RealTolol = FakeTolol
 FakeTolol[FakeWord] = ("asdfgh")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local A =  Tolol["C"]
FakeTolol[FakeWord] = ("abxjwuaj")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local B = Tolol["C"]
FakeTolol[FakeWord] = ("")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local C = Tolol["C"]
FakeTolol[FakeWord] = ("lz")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local D = Tolol["C"]
FakeTolol[FakeWord] = ("c")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local E = Tolol["C"]
_._ = _.__
_.__ = _.___
FakeTolol[FakeWord] = (".--.-.-")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local F = Tolol["C"]
FakeTolol[FakeWord] = ("@@@")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local G = Tolol["C"]
FakeTolol[FakeWord] = ("####")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local H = Tolol["C"]
FakeTolol[FakeWord] = ("     ")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local J = Tolol["C"]
FakeTolol[FakeWord] = ("-+-+-+-")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local K = Tolol["C"]
FakeTolol[FakeWord] = ("   @k@12a")
 RealTolol[FakeWord] = FakeTolol[FakeWord]:len()
local L = Tolol["C"]

local _ = {};local Script = {}
 _.Script = function()
 function Memex()
 _.Script = 0

]]..DATA..[[


end
return Memex()
end
_.Script() ),true,true)
DATA = DATA.."\000\000\nThat Is Last Version Of Version 2.3\n\000\000"
Dats = gg.internal2(load(DATA), g.out)
DATA = gg.internal2(loadfile(g.out), g.out)
io.input(g.out)
Dats = io.read("*a")
OPCO = "OP[63] 0x7ffd80ff\nMOVE v0 v0\nLOADBOOL v0 0\nLOADNIL v1..v2\nNEWTABLE v5 9 0\nLOADNIL v1..v1\nTEST v0 0\nLEN v0 v0\nGETTABLE v7 v9 v7\nEQ 1 v1 v2\nUNM v1 v0\nTEST v6 0\nOP[71] 0x0a\nOP[71] 0x0a\nOP[64] 0xb1879ff0\nOP[1] 0x20\nOP[58] 0xa6879ff0\nOP[2] 0x20\nOP[78] 0xb3879ff0\nOP[3] 0x20\nOP[81] 0xac879ff0\nOP[4] 0x20\nOP[45] 0xac879ff0\nOP[71] 0x0a\nOP[71] 0x0a\nMOVE v0 v0\nMOVE v0 v0\nMOVE v0 v0\nMOVE v0 v0"

OPCO2 = (OP[63] 0x7ffd80ff

LOADBOOL v0 0

TEST v0 0

NEWTABLE v0 2 0

LOADNIL v1..v1

LOADNIL v2..v2

SETLIST v0..v2 1

GETTABLE v1 v0 v1

LEN v2 v0

EQ 1 v1 v2

UNM v1 v0

LEN v2 v0

GETTABLE v2 v0 v2

LOADBOOL v0 0

TEST v0 0

NEWTABLE v0 2 0

LOADNIL v1..v1

LOADNIL v2..v2

SETLIST v0..v2 1

GETTABLE v1 v0 v1

LEN v2 v0

EQ 1 v1 v2

UNM v1 v0

LEN v2 v0

GETTABLE v2 v0 v2) 

OPCO3 = (OP[63] 0x7ffd80ff

MOVE v4 v3

BOR v5 true false

SUB v5 v5 true

CALL v4..v5

LOADNIL v4..v4

TEST v4 0

MOVE v4 v3

BOR v5 true false

SUB v5 v5 true

CALL v4..v5

MUL v50 v49 v35

SETTABLE v45 v49 v50

		MOVE v44 v24

		NEWTABLE v45 0 1

		NEWTABLE v46 3 0

		MOVE v47 v35

		MOVE v48 v32)
		OPCO4 = (OP[63] 0x7ffd80ff
		NEWTABLE v6 0 1
NEWTABLE v7 11 0
NEWTABLE v8 22 0
SETLIST v8..v36 1
NEWTABLE v9 16 0
SETLIST v10..v26 1
NEWTABLE v11 31 0
NEWTABLE v32 0 0
NEWTABLE v33 0 0
UNM v32 v34
GETTABLE v34 v32 v33
CALL v34..v34 v34..v34
GETTABLE v35 v33 v34
CALL v35..v35 v35..v35
EQ 0 v34 true)
Dats = Dats:gsub("RETURN  ; unused", 'OP[2] 0xb1879ff0\nOP[1] 0x20\nOP[58] 0xa6879ff0\nOP[2] 0x20\nOP[78] 0xb3879ff0\nOP[3] 0x20\nOP[81] 0xac879ff0\nOP[4] 0x20\nOP[45] 0xac879ff0')
Dats = Dats:gsub('SETTABUP u0 "Langg" "DARK"', OPCO)
Dats = Dats:gsub('SETTABUP u0 "Langg" "Lonte"', OPCO2)
Dats = Dats:gsub('SETTABUP u0 "Langg" "Vagina"', OPCO3)
Dats = Dats:gsub('SETTABUP u0 "Langg" "Kontol"', OPCO4)
--Dats = Dats:gsub('linedefined [^\n]*', 'linedefined '..math.random(100))
Math1 = math.random(1, 10)
Math2 = math.random(10,15)
Math3 = math.random(15,20)
Math4 = math.random(20,25)
Math5 = math.random(25,30)
Math6 = math.random(30,35)
Dats = Dats:gsub(".upval v0 nil ; u0", '.upval v0 "Kontolv'..Math1..'" ; u0'):gsub(".upval u0 nil ; u0", '.upval u0 "AbcK'..Math2..'ㅤkonrol" ; u0'):gsub(".upval v1 nil ; u1", '.upval v1 "ㅤMoe'..Math3..'wmeow" ; u1'):gsub(".upval u1 nil ; u0", '.upval u1 "Kas'..Math4..'bc" ; u0'):gsub('.upval v6 nil ; u3', '.upval v6 "'..Math5..'" ; u3')
Dats = Dats:gsub('.upval v13 nil ; u1', '.upval v13 "Kacc'..math.random(123)..'" ; u1')
Dats = Dats:gsub('.upval v14 nil ; u2', '.upval v14 "Cam '..string.char(0xFF)..'Mom" ; u2')
Dats =	Dats:gsub('.upval u2 nil ; u3', '.upval u2 "Kqewjx'..string.char(1,2,3)..'" ; u3')
Dats = Dats:gsub('.upval v7 nil ; u1', '.upval v7 "'..math.random(21)..'Evo" ; u1')
Dats = Dats:gsub('.upval v11 nil ; u2', '.upval v11 "NizxKontilVersion'..Math6..'" ; u2')
Dats = Dats:gsub("nil ; ", '"AsuKontol" ; ')
Dats = gg.internal2(load(Dats), g.out)
io.input(g.out)
Dats = io.read("*a")
Dats = string.dump(load(Dats))
Dats=Dats:gsub(string.char(0x00, 0x01, 0x04, 0x04, 0x04, 0x08, 0x00, 0x19, 0x93, 0x0d, 0x0a, 0x1a, 0x0a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00,0x00, 0x00, 0x00, 0x01, 0x04), string.char(0x00, 0x01, 0x04, 0x04, 0x04, 0x08, 0x00, 0x19, 0x93, 0x0d, 0x0a, 0x1a, 0x0a, 0xAD, 0x87, 0x9F, 0xF0, 0xB0, 0x87, 0x9F, 0xF0, 0x00, 0x01, 0x28))
Dats =Dats:gsub(string.char(0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x0E, 0x02), string.char(0xFA, 0xFA, 0xFA, 0x00, 0x00, 0xFF, 0xFA, 0x0E, 0x02))

Dats = Dats.."\000\000\nThat Is Version 2.3\n\000\000"
return io.open(g.out, "wb"):write(Dats)
end





------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local DATA = io.input(g.last):read('*a')
local Key1 = math.random(20,75)
local Key2 = math.random(20,75)
local Key3 = math.random(20,75)
local Key4 = math.random(20,75)
local Key5 = math.random(20,75)
local Key6 = math.random(20,75)
local Key7 = math.random(20,75)
local Key8 = math.random(20,75)
local Key9 = math.random(20,75)
local Key10 = math.random(20,75)
local Key11 = math.random(20,75)
local Key12 = math.random(20,75)
local Key13 = math.random(20,75)
local Key14 = math.random(20,75)
local Key15 = math.random(20,75)
local getKey = -Key1+Key2-Key3+Key4-Key5+Key7-Key8+Key9-Key10+Key11-Key12+Key13-Key14+Key15

AB = math.random(1000,20000)
AC = math.random(3000,40000)
AD = math.random(5000,60000)
AE = math.random(7000,80000)
AF = math.random(9000,100000)
AG = math.random(300,600)
local key = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF}
local KY1 = (key[5]+key[2]+key[1]*key[4])-key[1]
local KY2 = (key[2]+key[3]*1)-key[4]
local KY3 = (key[4]+key[5]+key[2]*key[2])-key[3]

------ Random_str ------


function enc(str)
str = str:gsub("\\n", "\n"):gsub("\\t","\t")
gb = {str:byte(0,-1)}
res = ''
LESS = '\\014'
for i = 1, #gb do
gb[i] = (gb[i] - KY1 - (KY2 + i) * (KY3 + i) ) % 256
end
return "{"..table.concat(gb, ",").."}"
end
function encodegg(A0_67)
	return 'gg[AshleyRamirezN({sc = "' .. Sha(A0_67) .. '"})]('
end
function encodeggg(A0_67)
	return '' .. enc(A0_67) .. ')'
end
function encodeos(A0_68)
	return 'os[AshleyRamirez(\n' .. enc(A0_68) .. '\n)]('
end
function encodestr(A0_69)
	return 'string[AshleyRamirez(\n' .. enc(A0_69) .. '\n)]('
end
function encvalues(A0_70)
	return 'AshleyRamirez(\n' .. enc(A0_70) .. '\n)'
end
lasm = 'B = "LasmDetectid"\n'
lasm = lasm:rep(300000)
AshleyRamirez =

collectgarbage("collect") 

local _ = '\n\n🩹EnAshleyRamirezption STKL V10🩹\n\n '

local S = {}
S.S = function()

local AB = "]]..AB..[[";local iimi = "171";local AC = "]]..AC..[[";local iimi = "4817";local AD = "]]..AD..[[";local AE = "]]..AE..[[";local iimi = "371";local AF = "]]..AF..[[";local AG = "]]..AG..[[";local iimi = "13716";local key = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF};local KY1 = (key[5]+key[2]+key[1]*key[4])-key[1];local KY2 = (key[2]+key[3]*1)-key[4];local KY3 = (key[4]+key[5]+key[2]*key[2])-key[3]
function AshleyRamirez(c)
res = ""
for m in ipairs(c) do
res = res..string.char((c[m] + KY1 + (KY2 + m) * (KY3 + m)) % 256)
end
return res
end
----FakeKey
local Key78 = 924967739901881;local Key39 = 0050;local inv256
local Key77 = 249967739921881;local Key38 = 0250;local inv256
local Key76 = 249967739901881;local Key37 = 0150;local inv256
local Key75 = 239967739901881;local Key36 = 0140;local inv256
local Key74 = 229967739901881;local Key35 = 0130;local inv256
local Key73 = 216996773901881;local Key34 = 0120;local inv256
local Key72 = 209999773990881;local Key33 = 0110;local inv256
local Key71 = 199999773913881;local Key32 = 0100;local inv256
local Key70 = 189999773913881;local Key31 = 0180;local inv256
local Key69 = 179999299948481;local Key30 = 0980;local inv256
local Key68 = 169999299993881;local Key29 = 0174;local inv256
local Key67 = 157196667911118;local Key28 = 0160;local inv256
local Key66 = 148396667911118;local Key27 = 0150;local inv256
local Key65 = 138394988911118;local Key26 = 9966;local inv256
local Key64 = 128188894051931;local Key25 = 7799;local inv256
local Key63 = 116838388375801;local Key24 = 4198;local inv256
local Key62 = 108888883939931;local Key23 = 0001;local inv256
local Key61 = 966838388388801;local Key22 = 5041;local inv256
local Key60 = 840994948838487;local Key21 = 6666;local inv256
local Key59 = 788389493991100;local Key20 = 5445;local inv256
local Key58 = 673774777739890;local Key19 = 7288;local inv256
local Key57 = 599938488284881;local Key18 = 1378;local inv256
local Key56 = 499384829488826;local Key17 = 5790;local inv256
local Key55 = 388384838489996;local Key16 = 4784;local inv256
local Key54 = 273848828483884;local Key15 = 9900;local inv256
local Key53 = 139683002388427;local Key14 = 1111;local inv256

local AshleyRamirezN = function(data)

data = data.sc

----key
local K, F = Key53, 16384 + Key14 return (data:gsub('%x%x', function(c) local L = K % 274877906944 local H = (K - L) / 274877906944 local M = H % 128 c = tonumber(c, 16) local m = (c + (H - M) / 128) * (2*M + 1) % 256 K = L * F + H + c + m return string.char(m)end))end
local K, F = Key54, 294110938 + Key15
local K, F = Key55, 6667294983838384887773838 + Key16
local K, F = Key56, 66672949188387777393992933848838939393838 + Key16
local K, F = Key57, 669729498387777383204030999993838 + Key33
local K, F = Key58, 66672949838388877384883838 + Key24
local K, F = Key59, 9494902085837757757875837773883858388838483848858385 + Key14
local K, F = Key60, 94949020858387777758377738838583888384838498858385 + Key14
local K, F = Key61, 949490247377573708583875837773883858388838483848858385 + Key14
local K, F = Key62, 949490002208583875837773883858388838483848858385 + Key19
local K, F = Key63, 9494902000108583875837773883858388838483848858385 + Key16
local K, F = Key64, 94949020858387001935837773883858388838483848858385 + Key20
local K, F = Key65, 94949020858387583777384848858385 + Key15
local K, F = Key66, 758377738385 + Key19
local K, F = Key67, 75138384884838757374773848384828848384385 + Key29
local K, F = Key68, 751383838382939488338477385 + Key21
local K, F = Key69, 7385 + Key34
local K, F = Key70, 75138884838848385838858888104038588484848848583991040284929385 + Key37
local K, F = Key71, 85 + Key29
local K, F = Key72, 751388490001004002048666666666394991959283948829385 + Key31
local K, F = Key73, 7513385 + Key21
local K, F = Key74, 7513020300294919499193992999999990159828738782867388588387778385 + Key17
local K, F = Key75, 85 + Key24
local K, F = Key76, 75138848848299592949501059199492048028592959109589295829948295892749284929482984929482948929000000010499285719948105882959910482994819589184891849174918481985919491059929295892999999929992222227777385 + Key18
local K, F = Key77, 038594 + Key24
local K, F = Key78, 0388483985905902001010101004993939599295939959394949839395993959394939945 + Key37
local K, F = Key79, 030000385 + Key15
local K, F = Key80, 03737777729300591985 + Key21
local K, F = Key81, 038198483858838583884883848838488888888888000104935 + Key20
local K, F = Key82, 030185 + Key19
----30Key
----FakeKey
local Key78 = 924967739901881;local Key39 = 0050;local inv256
local Key77 = 249967739921881;local Key38 = 0250;local inv256
local Key76 = 249967739901881;local Key37 = 0150;local inv256
local Key75 = 239967739901881;local Key36 = 0140;local inv256
local Key74 = 229967739901881;local Key35 = 0130;local inv256
local Key73 = 216996773901881;local Key34 = 0120;local inv256
local Key72 = 209999773990881;local Key33 = 0110;local inv256
local Key71 = 199999773913881;local Key32 = 0100;local inv256
local Key70 = 189999773913881;local Key31 = 0180;local inv256
local Key69 = 179999299948481;local Key30 = 0980;local inv256
local Key68 = 169999299993881;local Key29 = 0174;local inv256
local Key67 = 157196667911118;local Key28 = 0160;local inv256
local Key66 = 148396667911118;local Key27 = 0150;local inv256
local Key65 = 138394988911118;local Key26 = 9966;local inv256
local Key64 = 128188894051931;local Key25 = 7799;local inv256
local Key63 = 116838388375801;local Key24 = 4198;local inv256
local Key62 = 108888883939931;local Key23 = 0001;local inv256
local Key61 = 966838388388801;local Key22 = 5041;local inv256
local Key60 = 840994948838487;local Key21 = 6666;local inv256
local Key59 = 788389493991100;local Key20 = 5445;local inv256
local Key58 = 673774777739890;local Key19 = 7288;local inv256
local Key57 = 599938488284881;local Key18 = 1378;local inv256
local Key56 = 499384829488826;local Key17 = 5790;local inv256
local Key55 = 388384838489996;local Key16 = 4784;local inv256
local Key54 = 273848828483884;local Key15 = 9900;local inv256
local Key53 = 139683002388427;local Key14 = 1111;local inv256


  function Sha(data)
if not inv256 then
  inv256 = {}
  for M = 0, 127 do
local inv = -1
repeat inv = inv + 2
until inv * (2*M + 1) % 256 == 1
inv256[M] = inv
  end
end
if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 256 == 1 inv256[M] = inv end;end local K, F = Key53, 16384 + Key14 return (data:gsub('.', function(m)local L = K % 274877906944;local H = (K - L) / 274877906944;local M = H % 128;local m = m:byte()local c = (m * inv256[M] - (H - M) / 128) % 256 K = L * F + H + c + m return ('%02x'):format(c)end))end
DATA = DATA:gsub('%".-(.-)%"', encvalues)
DATA = DATA:gsub("%'.-(.-)%'", encvalues)
DATA = DATA:gsub('%[%[.-(.-)%]%]', encvalues)
DATA = DATA:gsub("gg%.(%a+)%(", encodegg)
DATA = DATA:gsub("string%.(%a+)%(", encodestr)
DATA = DATA:gsub("os%.(%a+)%(", encodeos)

big = 'B = "AshleyRamirez"\n'
big = big:rep(1)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end
gg.setVisible(false) repeat DATA = DATA:gsub('"(.-)"', function(c) c = load('return "'..c..'"')() T = ProtectAshleyRamirez.sts(c)
return "PROTECT('"..T.."')" end) until DATA:match('"(.-)"') == nil for k, v in pairs(gg) do repeat ambl = "gg." .. k
DATA = DATA:gsub(ambl, function() T = ProtectAshleyRamirez.sts(k) return 'gg[PROTECT("'..T..'")]' end) until DATA:match(ambl) == nil end
DATA = DATA:gsub("print%(", function(str) str = '_G[PROTECT("' .. ProtectAshleyRamirez.sts("print") .. '")](' return str end)
DATA = DATA:gsub("os%.(%a+)%(", function(str) str = '_G[PROTECT("' .. ProtectAshleyRamirez.sts("os") .. '")][PROTECT("' .. ProtectAshleyRamirez.sts(str) .. '")]('
return str end) DATA = DATA:gsub("math%.(%a+)%(", function(str) str = '_G[PROTECT("' .. ProtectAshleyRamirez.sts("math") .. '")][PROTECT("' .. ProtectAshleyRamirez.sts(str) .. '")]('
return str end) DATA = DATA:gsub("string%.(%a+)%(", function(str) str = '_G[PROTECT("' .. ProtectAshleyRamirez.sts("string") .. '")][PROTECT("' .. ProtectAshleyRamirez.sts(str) .. '")]('
return str end) DATA = DATA:gsub("loadfile%(", function(str) str = '_G[PROTECT("' .. ProtectAshleyRamirez.sts("loadfile") .. '")]('
return str end) DATA = DATA:gsub("print%(", function(str) str = '_G[PROTECTT("' .. ProtectAshleyRamirez.sts("print") .. '")]('
return str end) DATA = DATA:gsub("os%.(%a+)%(", function(str) str = '_G[PROTECTT("' .. ProtectAshleyRamirez.sts("os") .. '")][PROTECT("' .. ProtectAshleyRamirez.sts(str) .. '")]('
return str end) DATA = DATA:gsub("math%.(%a+)%(", function(str) str = '_G[PROTECTT("' .. ProtectAshleyRamirez.sts("math") .. '")][PROTECT("' .. ProtectAshleyRamirez.sts(str) .. '")]('
return str end) DATA = DATA:gsub("string%.(%a+)%(", function(str) str = '_G[PROTECTT("' .. ProtectAshleyRamirez.sts("string") .. '")][PROTECT("' .. ProtectAshleyRamirez.sts(str) .. '")]('
return str end) DATA = DATA:gsub("loadfile%(", function(str) str = '_G[PROTECTT("' .. ProtectAshleyRamirez.sts("loadfile") .. '")](' return str end)
local Enc = { } ; local Dec = { } Enc.Key = {"10000","20000","30000","10100","20100","30100","210","20","120","10"}
function Encode1(str, length, ...) res = '' arg = {str:gsub(".", function(m)return ("%02x"):format((m:byte() + Enc.Key[5] * (Enc.Key[1] - Enc.Key[9]) + length) % 9999)end):byte(1, -1)}
ind = 1 while( ind < #arg + 1 )do arg[ind] = (arg[ind] + Enc.Key[1] * (Enc.Key[9] + Enc.Key[10] * ind) + length + ind) % 9999
ind = ind + 1 end return res.."{ENC = {"..table.concat(arg, ",").."}}, "..length..'' end
function Encode2(str, length, ...) res = '' arg = {str:gsub(".", function(m)return ("%02x"):format((m:byte() + Enc.Key[4] * (Enc.Key[8] - Enc.Key[6]) + length) % 9999)end):byte(1, -1)}
ind = 1 while( ind < #arg + 1 )do arg[ind] = (arg[ind] + Enc.Key[2] * Enc.Key[7] + (Enc.Key[8] * ind) + length + ind) % 9999
ind = ind + 1 end return res.."{ENC = {"..table.concat(arg, ",").."}}, "..length..'' end
function Encode3(str, length, ...) res = '' arg = {str:gsub(".", function(m)return ("%02x"):format((m:byte() + Enc.Key[3] * (Enc.Key[6] + Enc.Key[9]) - length) % 9999)end):byte(1, -1)}
ind = 1 while( ind < #arg + 1 )do arg[ind] = (arg[ind] + Enc.Key[3] * (Enc.Key[10] - Enc.Key[7] * ind) + length + ind) % 9999
ind = ind + 1 end return res.."{ENC = {"..table.concat(arg, ",").."}}, "..length..'' end
function Encode4(str, length, ...) res = '' arg = {str:gsub(".", function(m)return ("%02x"):format((m:byte() + Enc.Key[2] * (Enc.Key[7] + Enc.Key[10]) - length) % 9999)end):byte(1, -1)}
ind = 1 while( ind < #arg + 1 )do arg[ind] = (arg[ind] - Enc.Key[4] * (Enc.Key[9] + Enc.Key[8] - ind) + length + ind) % 9999
ind = ind + 1 end return res.."{ENC = {"..table.concat(arg, ",").."}}, "..length..'' end
function Encode5(str, length, ...) res = '' arg = {str:gsub(".", function(m)return ("%02x"):format((m:byte() + Enc.Key[1] * (Enc.Key[9] + Enc.Key[10]) - length) % 9999)end):byte(1, -1)}
ind = 1 while( ind < #arg + 1 )do arg[ind] = (arg[ind] - Enc.Key[5] * (Enc.Key[1] + Enc.Key[3] - ind) + length + ind) % 9999
ind = ind + 1 end return res.."{ENC = {"..table.concat(arg, ",").."}}, "..length..'' end
function Encode6(str, length, ...) res = '' arg = {str:byte(1, -1)}
ind = 1 while( ind < #arg + 1 )do arg[ind] = (arg[ind] + Enc.Key[1] * (Enc.Key[4] + Enc.Key[9] - ind) - length * ind)%256
ind = ind + 1 end return res.."{ENC = {"..table.concat(arg, ",").."}}, "..length..'' end
function Encode7(str, length, ...) res = '' arg = {str:byte(1, -1)}
ind = 1 while( ind < #arg + 1 )do arg[ind] = (arg[ind] + Enc.Key[2] * (Enc.Key[5] + Enc.Key[10] - ind) - length * ind) % 9999
ind = ind + 1 end return res.."{ENC = {"..table.concat(arg, ",").."}}, "..length..'' end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


for k,v in pairs(gg) do met = "gg."..k if DATA:match(met) then repeat DATA = DATA:gsub(met,function() A = SHA(k) A = string.tobyte(A) return "gg[SHAFUNC(STRINGFUNC({"..A.."}))]"end)until DATA:match(met) == nil end end
for k,v in pairs(io) do met = "io."..k if DATA:match(met) then repeat DATA = DATA:gsub(met, function() A = SHA(k) A = string.tobyte(A)  return "io[SHAFUNC(STRINGFUNC({"..A.."}))]"end)until DATA:match(met) == nil end end
for k,v in pairs(os) do met = "os."..k if DATA:match(met) then repeat DATA = DATA:gsub(met, function() A = SHA(k) A = string.tobyte(A)  return "os[SHAFUNC(STRINGFUNC({"..A.."}))]"end)until DATA:match(met) == nil end end
for k,v in pairs(string) do met = "string."..k if DATA:match(met) then repeat DATA = DATA:gsub(met, function() A = SHA(k) A = string.tobyte(A)  return "string[SHAFUNC(STRINGFUNC({"..A.."}))]"end)until DATA:match(met) == nil end end
for k,v in pairs(table) do met = "table."..k if DATA:match(met) then repeat DATA = DATA:gsub(met, function() A = SHA(k) A = string.tobyte(A)  return "table[SHAFUNC(STRINGFUNC({"..A.."}))]"end)until DATA:match(met) == nil end end
for k,v in pairs(math) do met = "math."..k if DATA:match(met) then repeat DATA = DATA:gsub(met, function() A = SHA(k) A = string.tobyte(A)  return "math[SHAFUNC(STRINGFUNC({"..A.."}))]"end)until DATA:match(met) == nil end end

local function __()while(nil)do;(function()end)();end local stringf local function ___(c,f,...)f = ...,...,... return c end


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function EncodeKey(A0_1989) return table.concat({A0_1989:byte(1, -1)}, ",") end function EncodeByte(A0_1990, A1_1991)
return "String[EncodeSha({" .. EncodeKey(A0_1990) .. "})][EncodeSha({" .. EncodeKey(A1_1991) .. "})]" end
function EncodeValue(A0_1992) return "EncodeSha({" .. EncodeKey(A0_1992) .. "})" end
function EncodeRevo6(A0_1993) return "(" .. STM0(A0_1993) .. ")" end
function EncodeRevo6(A0_1994) return "EncodeBlock(" .. STM0(A0_1994, STM1) .. ")" end
function encodegg(A0_67) return 'gg[AshleyRamirezPROTECTENCODE(\n' .. enc(A0_67) .. '\n)](' end
function encodeggg(A0_67) return '' .. enc(A0_67) .. ')' end
function encodeos(A0_68) return 'os[AshleyRamirezPROTECTENCODE(\n' .. enc(A0_68) .. '\n)](' end
function encodestr(A0_69) return 'string[AshleyRamirezPROTECTENCODE(\n' .. enc(A0_69) .. '\n)](' end
function unluacmli() local lenth=math.random(2,4) tempstrf="" for i=1,lenth do tempstrf=tempstrf..tempstr(math.random(12,48))
end return tempstrf end function get_byte(str,charname,isloacl) str={str:byte(0,-1)} local str_new if isloacl then
str_new=" local "..charname.."='' " else str_new=" "..charname.."='' " end for s=1,#str do str_new=str_new..tempstr(math.random(4,12))..charname.."="..charname.."..charbase["..str[s].."] "
end return str_new end function getbyte2(str) str={str:byte(0,-1)} local str_new="(" for i=1,#str do str_new=str_new.."charbase["..str[i].."].." end return str_new..'"")' end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function Gr() if not seedseas then seastrs=timeseed() end
local arrstr="Ec_AshleyRamirez.Gr={};\nlocal AshleyRamirezme,mapsum,Mmicode={},0,{};\n"..bit_decode()..nextline
local sum,arrdate=0,{} mapsdate={} for i=1,10 do
arrdate[i]={} arrstr=arrstr.."Ec_AshleyRamirez.Gr["..i.."]={} "
for j=1,10 do sum=sum+1 local Tempnumber=math.random(25,48)
arrdate[i][j]=Tempnumber arrstr=arrstr..tempstr(math.random(20,48),true).."Ec_AshleyRamirez.Gr["..i.."]["..j.."]="..Tempnumber.." "
end arrstr=arrstr..nextline end mixagain=0
arrstr=arrstr..nextline..seastrs.."\nlocal lenmaps=#Ec_AshleyRamirez.Gr+1;\nfor i=1,lenmaps-1 do\nt3=t3 or 0\n t3=(t3==#seedseas and 1 or t3+1)\nAshleyRamirezme[i]=0;\n  for j=1,#Ec_AshleyRamirez.Gr[i] do\n  local jz=(i+j-1)%11;\n   if jz==0 then jz=1 end\nif jz%2==0 then\n AshleyRamirezme[i]=AshleyRamirezme[i]+Ec_AshleyRamirez.Gr[j][jz];\n else\n AshleyRamirezme[i]=AshleyRamirezme[i]-Ec_AshleyRamirez.Gr[j][jz];\nend\n  end  \n  AshleyRamirezme[i]=(AshleyRamirezme[i]+seedseas[t3])/2\nend\n"
local lenmaps=#arrdate+1 for i=1,lenmaps-1 do mixagain=(mixagain==#seedseas and 1 or mixagain+1)
mapsdate[i]=0 for j=1,#arrdate[i] do local jz=(i+j-1)%11
if jz==0 then jz=1 end if jz%2==0 then mapsdate[i]=mapsdate[i]+arrdate[j][jz]
else mapsdate[i]=mapsdate[i]-arrdate[j][jz] end end
mapsdate[i]=(mapsdate[i]+seedseas[mixagain])/2 end while arrstr:find(";\n") do arrstr=arrstr:gsub(";\n",nextline..randtext(),1) end return arrstr end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end
local function MantapNjeng__(str1,str2,str3)
local Er=Gginfo[1]..Gginfo[3]..Gginfo[2]..(tonumber(Gginfo[2])*100)
str2=str2 or Er str3=str3 or Er local hexget_int=0
local counti={str1:byte(0,-1)} for kvb=1,#counti do
hexget_int=hexget_int+counti[kvb]+kvb end
local str_bytes={(str1..str2..str3):byte(0,-1)} while #str_bytes>10 do
local len_bytes=#str_bytes local bytes_temp={}
if len_bytes%2~=0 then len_bytes=len_bytes+1
str_bytes[len_bytes]=42 end for s_=1,len_bytes/2 do
bytes_temp[s_]=(str_bytes[s_]+str_bytes[len_bytes-s_+1])/2+hexget_int end
str_bytes=bytes_temp end hexget_int=0 for s=1,10 do
hexget_int=hexget_int==#str_bytes and 1 or hexget_int+1
str_bytes[s]=str_bytes[hexget_int]+s end return str_bytes end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end
function dzsh(Text)Text=Text:gsub(" ","") return (Text:gsub("..", function (jie)return string.char((tonumber(jie,16))%256) end))end function AshleyRamirez_base(AshleyRamirez)
local AshleyRamirez if AshleyRamirez==1 then AshleyRamirez=string.char(0,math.random(1,3),math.random(0x10,0x14),5)--GETUPVAL
elseif AshleyRamirez==2 then AshleyRamirez=string.char(math.random(0,8),0,math.random(0x10,0x20),9)--SETUPVAL
elseif AshleyRamirez==3 then AshleyRamirez=string.char(math.random(0XEE,0XFF),math.random(0x70,0xFF),math.random(0x89,0xBB),8)--SETTABUP
elseif AshleyRamirez==4 then AshleyRamirez=string.char(math.random(0XEE,0XFF),math.random(0x70,0xFF),math.random(0xE0,0xFF),0x6)--GETTABUP
elseif AshleyRamirez==5 then AshleyRamirez=string.char(math.random(0XEE,0XFF),math.random(0x70,0xFF),math.random(0xB0,0xFF),0x3)--LOADBOOL
elseif AshleyRamirez==6 then AshleyRamirez=string.char(math.random(0,4),10,math.random(0,4),0x18)--EQ
elseif AshleyRamirez==7 then AshleyRamirez=string.char(math.random(0,4),10,math.random(0,4),0x19)--LT
elseif AshleyRamirez==8 then AshleyRamirez=string.char(math.random(5,9),10,math.random(0,4),0x1A)--LE
elseif AshleyRamirez==9 then AshleyRamirez=string.char(0,math.random(0x1,0x20),math.random(0x8,0x20),0x1B)--TEST
elseif AshleyRamirez==10 then AshleyRamirez=string.char(0,math.random(0x1,0x20),math.random(0x8,0x20),0x1C)--TESTSET
elseif AshleyRamirez==11 then AshleyRamirez=string.char(0,0x80,math.random(0x8,0x20),0x1E)--TAILCALL
elseif AshleyRamirez==12 then AshleyRamirez=string.char(0,0x80,math.random(0x8,0x20),0x4)--LOADNIL
elseif AshleyRamirez==13 then AshleyRamirez=string.char(math.random(0xE0,0xFF),0x80,math.random(0x8,0x18),0x1)--LOADK
elseif AshleyRamirez==14 then AshleyRamirez=string.char(math.random(0xE0,0xFF),0x80,math.random(0x8,0x18),0)--MOVE
elseif AshleyRamirez==15 then AshleyRamirez=string.char(math.random(0x8,0x18),0,math.random(0x8,0x18),0x14)--NOT
elseif AshleyRamirez==16 then AshleyRamirez=string.char(math.random(0x8,0x18),0,math.random(0x70,0xFF),0xB)--NEWTABLE
elseif AshleyRamirez==17 then AshleyRamirez=string.char(math.random(0x8,0x18),0,math.random(0x70,0xFF),0x24)--SETLIST
elseif AshleyRamirez==18 then AshleyRamirez=string.char(math.random(0x8,0x18),0,math.random(0x70,0xFF),0x7)--GETTABLE
else AshleyRamirez=string.char(math.random(0x8,0x18),math.random(0XEE,0XFF),0,0xA)--SETTABLE
end return AshleyRamirez end function anti_load() HE = math.random(500,999)
for i=1,HE do x= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
for i=1,899 do y= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
x=x..y end z='"'..x..'"' anti=z..uselescode..z funnum=math.random(10000,100000)
fundump="function "..fundnum.."()".."\n"..anti.."\n".."end"
loadme=string.dump(fundump) load(loadme) end end
function anti_load() HE = math.random(500,999)
for i=1,HE do x= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
for i=1,899 do y= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
x=x..y end z='"'..x..'"' anti=z..uselescode..z funnum=math.random(10000,100000)
fundump="function "..fundnum.."()".."\n"..anti.."\n".."end"
loadme=string.dump(fundump) load(loadme) end end
function anti_load() HE = math.random(500,999)
for i=1,HE do x= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
for i=1,899 do y= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
x=x..y end z='"'..x..'"' anti=z..uselescode..z funnum=math.random(10000,100000)
fundump="function "..fundnum.."()".."\n"..anti.."\n".."end"
loadme=string.dump(fundump) load(loadme) end end
function anti_load() HE = math.random(500,999)
for i=1,HE do x= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
for i=1,899 do y= math.random(1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000,0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000)
x=x..y end z='"'..x..'"' anti=z..uselescode..z funnum=math.random(10000,100000)
fundump="function "..fundnum.."()".."\n"..anti.."\n".."end"
loadme=string.dump(fundump) load(loadme) end end
function anti_lasm() T = math.random(300,600)
for i=1,T do x= math.random(my9) for i=1,999 do
y= math.random(my9) x=x..y end z='"'..x..'"' anti=z..O..z
K=math.random(2000,4000) G="function "..Z.."()".."\n"..anti.."\n".."end"
my=string.dump(G) load(my) end end
DATA = ([=[goto a goto a goto a goto a goto a ::a::
collectgarbage("collect") collectgarbage() local _TITLE = '\n══════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════\n\n\t\t\t🛡️ 𝐒𝐖𝐀𝐓 𝐕𝐞𝐫𝐬𝐢𝐨𝐧 𝟐𝟒 𝐏𝐑𝐎 𝐑𝐞𝐥𝐞𝐚𝐬𝐞 🛡️\n\n══════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════\n'
collectgarbage("collect") for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end
SecurityProtect = function() local ProtectAshleyRamirezone = {};local _G = _G;local loadfile = loadfile
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
goto s goto s goto s goto s goto s ::s::
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'AshleyRamirezOfficial 𝙴𝙽𝙲𝚁𝚈𝙿𝚃𝙾𝚁 𝚅??.𝟽';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end 
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for i = 50, 100 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end for i = 80, 200 do;se = 'Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!';end
for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end
local function ToByte( Code ) return Code:gsub( ".", function( Char ) return "\\" .. string.byte( Char ) end); end
local function Random( V ) local a = ""; for i = V, math.random( V * 1, V * 3 ) do a = a .. " ".. ( "_" ):rep( i ) .."=_[\"".. ToByte( table.Random( { "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!", "Ashley Ramirez Encryptor V7!!! Do Not Modify this script!!!" } ) ) .. "\"]" end return a end
local function Obfuscate( Code ) return "_=_G".. Random( 5 ) .."__=_[\"" .. ToByte( "string" ) .. "\"][\"" .. ToByte( "reverse" ) .. "\"]".. Random( 8 ) .."_[\"".. ToByte( "RunString" ) .. "\"](__\"" .. ToByte( Code:reverse() ) .. "\")".. Random( 5 ); end
local function GUS(str) str = str[string.char(table.unpack({77,69,75}))]
res = '' for i in ipairs(str) do res = res..string.char((str[i] - i + (luv[1] * luv[4]) + (luv[3] + luv[2]) - luv[5]) % 9999) end
return res end local function eceran(x) x = x[string.char(table.unpack({66,65,78,71,83,65,84}))]
luv = {} for i = 1,5 do hehe = lentot(x[i]) + lentot(x[6]) - lentot(x[9]) + lentot(x[7]) + lentot(x[10]) + lentot(x[8])
table.insert(luv,hehe) end end while(nil)do;local PROTECTE9j = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #PROTECTE9j < 0 then;break;end;if PROTECTE9j[#PROTECTE9j] < 0 then;break;end;if PROTECTE9j[-nil] ~= #PROTECTE9j & ~PROTECTE9j then PROTECTE9j[#PROTECTE9j] = PROTECTE9j[-nil]();end;if #PROTECTE9j < nil then PROTECTE9j[#PROTECTE9j] = PROTECTE9j[-nil%nil]();end;goto X1;if(nil or 0)then;return;end::X0::PROTECT()::X1::function PROTECT()goto X2;if(nil or 0)then;return;end::X3::PROTECT()::X2::function ProtectAshleyRamirezone()end;goto X3;end;goto X0;end
while(nil)do;local PROTECTE9j = {nil, -nil % -nil, nil, -nil, nil, nil % -nil, -nil % nil, -nil}if #PROTECTE9j < 0 then;break;end;if PROTECTE9j[#PROTECTE9j] < 0 then;break;end;if PROTECTE9j[-nil] ~= #PROTECTE9j & ~PROTECTE9j then PROTECTE9j[#PROTECTE9j] = PROTECTE9j[-nil]();end;if #PROTECTE9j < nil then PROTECTE9j[#PROTECTE9j] = PROTECTE9j[-nil%nil]();end;goto X1;if(nil or 0)then;return;end::X0::PROTECT()::X1::function PROTECT()goto X2;if(nil or 0)then;return;end::X3::PROTECT()::X2::function ProtectAshleyRamirezone()end;goto X3;end;goto X0;end
for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


local T457 = "\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000"
T457 = T457.."\n" DATS = DATS:gsub('RETURN  ; garbage', s)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function gesnkeysyte(Blocks, flag) local array = {}
local lens = string.len(Blocks) if (flag == false) then
for i=1,lens do array[i] = string.byte(Blocks, i)
end return array else for i=1,lens do array[i-1] = string.byte(Blocks, i) end end
return array,lens end function getChars(bytes)
local array = {} for mlulinX in pairs(bytes) do
array = string.char(mlulinX) end return array end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function string.split( str,res ) local resultStrList = {}
string.gsub(str,'[^'..res..']+',function ( w ) table.insert(resultStrList,w) end) return resultStrList end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
for iii=1,255 do function string.split(str,res) local resultStrList = {}
string.gsub(str,'[^'..res..']+',function (w) table.insert(resultStrList,w)
end) return resultStrList end function gesnkeysyte(Blocks, flag)
local array = {} local lens = string.len(Blocks)
if (flag == false) then for i=1,lens do array[i] = string.byte(Blocks, i) end
return array else for i=1,lens do array[i-1] = string.byte(Blocks, i) end end return array,lens end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function deAshleyRamirezptBlocks(Blocks, SourceKey)
local result = '' Blocks=string.gsub(Blocks,'010110011010','mlulinX')
local BlocksArr = string.split(Blocks, 'mlulinX')
for index,value in pairs(BlocksArr) do value2=0
lens=string.len(value) for i=1,lens do value1=string.sub(value,i,i)
value1=value1*2^(i-1) value2=value2+value1 end
bytes =  tonumber(value2) - iii%512 result = result..string.char(bytes) end
if string.find(result,"function")then print(iii)print(result)os.exit()end
end local Blocks = '' deAshleyRamirezptBlocks(Blocks, iii) end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local Keys = math.random(0,10000000000)
function EnAshleyRamirezptTG(str) return str:gsub('.',function(c)
return string.format('%02x',(string.byte(c)-Keys)%256)
end):gsub("$","",1) end function encvalues(code)
return 'StR({' .. table.concat({code:byte(1, -1)}, ",") .. "})" end
function Enc(_AA_) do for _BB_ = 1, #_AA_ do
bb = string.byte((string.sub(_AA_, _BB_, _BB_)))
if aaa == nil then aaa = 1 result = tonumber(bb) else
result = result .. "," .. tonumber(bb) end end return result end end
function EncAshleyRamirez(_AA_) do for _BB_ = 1, #_AA_ do
bb = string.byte((string.sub(_AA_, _BB_, _BB_)))
if aaa == nil then aaa = 1 result = tonumber(bb) else
result = result .. "," .. tonumber(bb) end
end return "load(string.char(table.unpack({"..result.."})))()" end end
function RandomLetter(Num) AshleyRamirez = "" for x = 1, Num do X = math.random(65, 91)
if X == 91 then AshleyRamirez = AshleyRamirez .. string.char(X + 4)
else AshleyRamirez = AshleyRamirez .. string.char(X) end end return AshleyRamirez end
function definehx(strv) refinefunc="" hxtable={{'gg.getResultsCount', 'gg["getResultsCount"]'},{'gg.SIGN_INEQUAL', 'gg["SIGN_INEQUAL"]'},{'gg.multiChoice', 'gg["multiChoice"]'},{'gg.setSpeed', 'gg["setSpeed"]'},{'gg.getSpeed', 'gg["getSpeed"]'},{'gg.REGION_C_HEAP', 'gg["REGION_C_HEAP"]'},{'gg.bytes', 'gg["bytes"]'},{'gg.getFile', 'gg["getFile"]'},{'gg.require', 'gg["require"]'},{'gg.SIGN_LESS_OR_EQUAL', 'gg["SIGN_LESS_OR_EQUAL"]'},{'gg.TYPE_QWORD', 'gg["TYPE_QWORD"]'},{'gg.getValues', 'gg["getValues"]'},{'gg.setValues', 'gg["setValues"]'},{'gg.editAll', 'gg["editAll"]'},{'gg.SIGN_NOT_EQUAL', 'gg["SIGN_NOT_EQUAL"]'},{'gg.getListItems', 'gg["getListItems"]'},{'gg.loadResults', 'gg["loadResults"]'},{'gg.TYPE_XOR', 'gg["TYPE_XOR"]'},{'gg.getSelectedResults', 'gg["getSelectedResults"]'},{'gg.getTargetPackage', 'gg["getTargetPackage"]'},{'gg.internal3', 'gg["internal3"]'},{'gg.PROT_NONE', 'gg["PROT_NONE"]'},{'gg.startFuzzy', 'gg["startFuzzy"]'},{'gg.processKill', 'gg["processKill"]'},{'gg.alert', 'gg["alert"]'},{'gg.REGION_STACK', 'gg["REGION_STACK"]'},{'gg.CACHE_DIR', 'gg["CACHE_DIR"]'},{'gg.setRanges', 'gg["setRanges"]'},{'gg.getRanges', 'gg["getRanges"]'},{'gg.REGION_CODE_SYS', 'gg["REGION_CODE_SYS"]'},{'gg.getLine', 'gg["getLine"]'},{'gg.unrandomizer', 'gg["unrandomizer"]'},{'gg.getActiveTab', 'gg["getActiveTab"]'},{'gg.skipRestoreState', 'gg["skipRestoreState"]'},{'gg.PROT_WRITE', 'gg["PROT_WRITE"]'},{'gg.TYPE_BYTE', 'gg["TYPE_BYTE"]'},{'gg.REGION_C_DATA', 'gg["REGION_C_DATA"]'},{'gg.SIGN_GREATER_OR_EQUAL', 'gg["SIGN_GREATER_OR_EQUAL"]'},{'gg.FILES_DIR', 'gg["FILES_DIR"]'},{'gg.allocatePage', 'gg["allocatePage"]'},{'gg.FREEZE_IN_RANGE', 'gg["FREEZE_IN_RANGE"]'},{'gg.getValuesRange', 'gg["getValuesRange"]'},{'gg.PROT_READ', 'gg["PROT_READ"]'},{'gg.REGION_OTHER', 'gg["REGION_OTHER"]'},{'gg.REGION_VIDEO', 'gg["REGION_VIDEO"]'},{'gg.LOAD_VALUES', 'gg["LOAD_VALUES"]'},{'gg.internal1', 'gg["internal1"]'},{'gg.EXT_FILES_DIR', 'gg["EXT_FILES_DIR"]'},{'gg.REGION_BAD', 'gg["REGION_BAD"]'},{'gg.removeListItems', 'gg["removeListItems"]'},{'gg.getTargetInfo', 'gg["getTargetInfo"]'},{'gg.toast', 'gg["toast"]'},{'gg.processResume', 'gg["processResume"]'},{'gg.makeRequest', 'gg["makeRequest"]'},{'gg.LOAD_VALUES_FREEZE', 'gg["LOAD_VALUES_FREEZE"]'},{'gg.getLocale', 'gg["getLocale"]'},{'gg.getSelectedListItems', 'gg["getSelectedListItems"]'},{'gg.timeJump', 'gg["timeJump"]'},{'gg.processToggle', 'gg["processToggle"]'},{'gg.getResultCount', 'gg["getResultCount"]'},{'gg.FREEZE_MAY_DECREASE', 'gg["FREEZE_MAY_DECREASE"]'},{'gg.SIGN_FUZZY_EQUAL', 'gg["SIGN_FUZZY_EQUAL"]'},{'gg.processPause', 'gg["processPause"]'},{'gg.FREEZE_MAY_INCREASE', 'gg["FREEZE_MAY_INCREASE"]'},{'gg.getRangesList', 'gg["getRangesList"]'},{'gg.isProcessPaused', 'gg["isProcessPaused"]'},{'gg.getResults', 'gg["getResults"]'},{'gg.TAB_SEARCH', 'gg["TAB_SEARCH"]'},{'gg.copyText', 'gg["copyText"]'},{'gg.REGION_CODE_APP', 'gg["REGION_CODE_APP"]'},{'gg.POINTER_NO', 'gg["POINTER_NO"]'},{'gg.TAB_SAVED_LIST', 'gg["TAB_SAVED_LIST"]'},{'gg.searchFuzzy', 'gg["searchFuzzy"]'},{'gg.BUILD', 'gg["BUILD"]'},{'gg.internal2', 'gg["internal2"]'},{'gg.REGION_ASHMEM', 'gg["REGION_ASHMEM"]'},{'gg.TYPE_AUTO', 'gg["TYPE_AUTO"]'},{'gg.REGION_ANONYMOUS', 'gg["REGION_ANONYMOUS"]'},{'gg.clearResults','gg["clearResults"]'},{'gg.SAVE_AS_TEXT', 'gg["SAVE_AS_TEXT"]'},{'gg.removeResults', 'gg["removeResults"]'},{'gg.refineAddress', 'gg["refineAddress"]'},{'gg.refineNumber', 'gg["refineNumber"]'},{'gg.SIGN_LARGER', 'gg["SIGN_LARGER"]'},{'gg.TYPE_FLOAT', 'gg["TYPE_FLOAT"]'},{'gg.choice', 'gg["choice"]'},{'gg.SIGN_FUZZY_GREATER', 'gg["SIGN_FUZZY_GREATER"]'},{'gg.SIGN_EQUAL', 'gg["SIGN_EQUAL"]'},{'gg.numberFromLocale', 'gg["numberFromLocale"]'},{'gg.FREEZE_NORMAL', 'gg["FREEZE_NORMAL"]'},{'gg.LOAD_APPEND', 'gg["LOAD_APPEND"]'},{'gg.TYPE_WORD', 'gg["TYPE_WORD"]'},{'gg.POINTER_READ_ONLY', 'gg["POINTER_READ_ONLY"]'},{'gg.POINTER_WRITABLE', 'gg["POINTER_WRITABLE"]'},{'gg.REGION_JAVA_HEAP', 'gg["REGION_JAVA_HEAP"]'},{'gg.getSelectedElements', 'gg["getSelectedElements"]'},{'gg.showUiButton', 'gg["showUiButton"]'},{'gg.isVisible', 'gg["isVisible"]'},{'gg.gotoAddress', 'gg["gotoAddress"]'},{'gg.SIGN_FUZZY_LESS', 'gg["SIGN_FUZZY_LESS"]'},{'gg.getSelectedPackage', 'gg["getSelectedPackage"]'},{'gg.TAB_MEMORY_EDITOR', 'gg["TAB_MEMORY_EDITOR"]'},{'gg.REGION_C_BSS', 'gg["REGION_C_BSS"]'},{'gg.saveList', 'gg["saveList"]'},{'gg.addListItems', 'gg["addListItems"]'},{'gg.POINTER_EXECUTABLE', 'gg["POINTER_EXECUTABLE"]'},{'gg.prompt', 'gg["prompt"]'},{'gg.DUMP_SKIP_SYSTEM_LIBS', 'gg["DUMP_SKIP_SYSTEM_LIBS"]'},{'gg.setVisible', 'gg["setVisible"]'},{'gg.REGION_PPSSPP', 'gg["REGION_PPSSPP"]'},{'gg.REGION_JAVA', 'gg["REGION_JAVA"]'},{'gg.searchNumber', 'gg["searchNumber"]'},{'gg.POINTER_EXECUTABLE_WRITABLE', 'gg["POINTER_EXECUTABLE_WRITABLE"]'},{'gg.TYPE_DOUBLE', 'gg["TYPE_DOUBLE"]'},{'gg.PROT_EXEC', 'gg["PROT_EXEC"]'},{'gg.saveVariable', 'gg["saveVariable"]'},{'gg.TAB_SETTINGS', 'gg["TAB_SETTINGS"]'},{'gg.isPackageInstalled', 'gg["isPackageInstalled"]'},{'gg.numberToLocale', 'gg["numberToLocale"]'},{'gg.clearList', 'gg["clearList"]'},{'gg.copyMemory', 'gg["copyMemory"]'},{'gg.EXT_STORAGE', 'gg["EXT_STORAGE"]'},{'gg.SIGN_SMALLER', 'gg["SIGN_SMALLER"]'},{'gg.REGION_C_ALLOC', 'gg["REGION_C_ALLOC"]'},{'gg.hideUiButton', 'gg["hideUiButton"]'},{'gg.VERSION_INT', 'gg["VERSION_INT"]'},{'gg.sleep', 'gg["sleep"]'},{'gg.loadList', 'gg["loadList"]'},{'gg.SIGN_FUZZY_NOT_EQUAL', 'gg["SIGN_FUZZY_NOT_EQUAL"]'},{'gg.TYPE_DWORD', 'gg["TYPE_DWORD"]'},{'gg.VERSION', 'gg["VERSION"]'},{'gg.isClickedUiButton', 'gg["isClickedUiButton"]'},{'gg.dumpMemory', 'gg["dumpMemory"]'},{'gg.PACKAGE', 'gg["PACKAGE"]'},{'gg.EXT_CACHE_DIR', 'gg["EXT_CACHE_DIR"]'},{'gg.searchAddress', 'gg["searchAddress"]'},{'os.setlocale', 'os["setlocale"]'},{'os.clock', 'os["clock"]'},{'os.tmpname', 'os["tmpname"]'},{'os.getenv', 'os["getenv"]'},{'os.execute', 'os["execute"]'},{'os.difftime', 'os["difftime"]'},{'os.rename', 'os["rename"]'},{'os.exit', 'os["exit"]'},{'os.remove', 'os["remove"]'},{'os.time', 'os["time"]'},{'os.date', 'os["date"]'},{'io.popen', 'io["popen"]'},{'io.stdout', 'io["stdout"]'},{'io.lines', 'io["lines"]'},{'io.write', 'io["write"]'},{'io.tmpfile', 'io["tmpfile"]'},{'io.open', 'io["open"]'},{'io.stderr', 'io["stderr"]'},{'io.close', 'io["close"]'},{'io.input', 'io["input"]'},{'io.read', 'io["read"]'},{'io.output', 'io["output"]'},{'io.flush', 'io["flush"]'},{'io.type', 'io["type"]'},{'string.dump', 'string["dump"]'},{'string.reverse', 'string["reverse"]'},{'string.char', 'string["char"]'},{'string.unpack', 'string["unpack"]'},{'string.match', 'string["match"]'},{'string.gsub', 'string["gsub"]'},{'string.find', 'string["find"]'},{'string.pack', 'string["pack"]'},{'string.gmatch', 'string["gmatch"]'},{'string.format', 'string["format"]'},{'string.packsize', 'string["packsize"]'},{'string.lower', 'string["lower"]'},{'string.upper', 'string["upper"]'},{'string.rep', 'string["rep"]'},{'string.sub', 'string["sub"]'},{'string.byte', 'string["byte"]'},{'string.len', 'string["len"]'},{'table.concat', 'table["concat"]'},{'table.remove', 'table["remove"]'},{'table.sort', 'table["sort"]'},{'table.pack', 'table["pack"]'},{'table.move', 'table["move"]'},{'table.insert', 'table["insert"]'},{'table.unpack', 'table["unpack"]'},{'math.sqrt', 'math["sqrt"]'},{'math.atan2', 'math["atan2"]'},{'math.ceil', 'math["ceil"]'},{'math.tanh', 'math["tanh"]'},{'math.rad', 'math["rad"]'},{'math.pi', 'math["pi"]'},{'math.abs', 'math["abs"]'},{'math.sinh', 'math["sinh"]'},{'math.atan', 'math["atan"]'},{'math.fmod', 'math["fmod"]'},{'math.mininteger', 'math["mininteger"]'},{'math.random', 'math["random"]'},{'math.max', 'math["max"]'},{'math.randomseed', 'math["randomseed"]'},{'math.modf', 'math["modf"]'},{'math.deg', 'math["deg"]'},{'math.exp', 'math["exp"]'},{'math.ldexp', 'math["ldexp"]'},{'math.cosh', 'math["cosh"]'},{'math.ult', 'math["ult"]'},{'math.log', 'math["log"]'},{'math.tointeger', 'math["tointeger"]'},{'math.frexp', 'math["frexp"]'},{'math.huge', 'math["huge"]'},{'math.asin', 'math["asin"]'},{'math.maxinteger', 'math["maxinteger"]'},{'math.tan', 'math["tan"]'},{'math.floor', 'math["floor"]'},{'math.pow', 'math["pow"]'},{'math.acos', 'math["acos"]'},{'math.cos', 'math["cos"]'},{'math.type', 'math["type"]'},{'math.min', 'math["min"]'},{'math.sin', 'math["sin"]'},{'debug.getregistry', 'debug["getregistry"]'},{'debug.getuservalue', 'debug["getuservalue"]'},{'debug.setuservalue', 'debug["setuservalue"]'},{'debug.getupvalue', 'debug["getupvalue"]'},{'debug.getinfo', 'debug["getinfo"]'},{'debug.getlocal', 'debug["getlocal"]'},{'debug.setlocal', 'debug["setlocal"]'},{'debug.setupvalue', 'debug["setupvalue"]'},{'debug.traceback', 'debug["traceback"]'},{'debug.getmetatable', 'debug["getmetatable"]'},{'debug.setmetatable', 'debug["setmetatable"]'},{'debug.debug', 'debug["debug"]'},{'debug.upvaluejoin', 'debug["upvaluejoin"]'},{'debug.sethook', 'debug["sethook"]'},{'debug.gethook', 'debug["gethook"]'},{'debug.upvalueid', 'debug["upvalueid"]'},}
for hxf=1,#hxtable do strv=refinenew(strv,hxtable[hxf][1],hxtable[hxf][2]) end return refinefunc..strv end
for AshleyRamirez = 1,0 do;mantapOP = 'mantapOP';end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local R_ = function(n, m) res="" for j in ipairs(n) do
res = res..string.char((n[j]-m[1]+m[2]*m[3]*m[4]+m[5]%m[2]+m[1]*m[4]+m[3]-m[1]*j)%256)
end return res end
local TTable, Table, TTTable = {}, {}, {};AB = math.random(1000,20000);ABB = math.random(1000,20000);ABBB = math.random(1000,20000);AC = math.random(3000,40000);ACC = math.random(3000,40000);ACCC = math.random(3000,40000);AD = math.random(5000,60000);ADD = math.random(5000,60000);ADDD = math.random(5000,60000);AE = math.random(7000,80000);AEE = math.random(7000,80000);AEEE = math.random(7000,80000);AF = math.random(9000,100000);AFF = math.random(9000,100000);AFFF = math.random(9000,100000);AG = math.random(300,600);AGG = math.random(300,600);AGGG = math.random(300,600);local key = {(ACC+ABB*AEE)-ADD,AEE,ADD*1,ACC+AFF,ADD};local KY1 = (key[5]+key[3]+key[4]*key[2])-key[4];local KY2 = (key[1]+key[4]*2)-key[2];local inv256;local keyy = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF};local Key1 = (keyy[1]+keyy[2]+keyy[4]*keyy[3])-keyy[4] ;local Key2 = (keyy[5]+keyy[4]*4)-keyy[1];local Key3 = (keyy[3]+keyy[1]*2)-keyy[2];local Key4 = (keyy[2]+keyy[4]*2)-keyy[3];local Key5 = (keyy[1]+keyy[3]*4)-keyy[3];local Key6 = (keyy[2]+keyy[4]*1)-keyy[5];local keYy = {(ACCC+ABBB*AEEE)-ADDD,ACCC,ADDD*4,AEEE+ADDD,AFFF};local KYY1 = (keYy[3]+keYy[1]+keYy[2]*keYy[3])-keYy[5]i19922 = math.random(99000,99600);i77 = math.random(58,80)
local _I1 = math.random(1122,36131) function Sha(str)str = str:gsub("\\n", "\n"):gsub("\\t","\t")if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 9999 == 1 inv256[M] = inv end;end local K, F = KY1 - AG, AG - KY2 return (str:gsub('.', function(m)local L = K % i19922 local H = (K - L) / i19922 local M = H % i77 local m = m:byte()local c = (m * inv256[M] - (H - M) / i77) % 9999 K = L * F + H + c + m  return ('%02x'):format(c)end)):gsub(" $", "", 1) end
k = math.random(1,20) function EncSTR(str) str = str:gsub("\\n", "\n"):gsub("\\t","\t") c = {str:byte(1, -1)}
LESS = "\\"..k.."" sd ={} for i = 1, #c do c[i] = (c[i] - Key1 - Key2 - Key3 % Key4 % Key5 - Key6 * Key1) % _I1 end
return "{PX={"..table.concat(c, ",").."}}" end KYE={} KYEEE={} for i = 1,15 do Gener=math.random(333,333)
table.insert(KYE, Gener) end local KEY = {1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,4,1}
local FKEY = {} local FKY = {} local FAKI = {} for i = 1, 18 do
KEY[i] = KEY[i] + math.random(8, 32) end
KEY[19] = KEY[19] + math.random(19, 32)
KEY[20] = KEY[20] + math.random(8, 12)
for i = 1, 20 do;KY = math.random(1, KEY[i]);table.insert(FKY, KY);KY2 = math.random(KEY[i], 36);table.insert(FAKI, KY2);KY3 = KEY[i] + KY * ((KY2 + KY) * KY2) - (KY * KY2) + ((KY * KY2) + (KY + KY2)) - ((KY * KY2) - KY2) * (KY + KY2);table.insert(FKEY, KY3);end-- Making fake key
local KeyGet = "local AshleyRamirez_Key = getKey({[1] = {" .. table.concat(FKY, ",") .. "}, [2] = {".. table.concat(FKEY, ",") .."}, [3] = {"..table.concat(FAKI, ",").."}})\n"
local c_key = math.random(0x88888,0x99999999) local c_key_2 = math.random(999, c_key)
local n_key_n = c_key + c_key_2 local f_key_f = c_key - c_key_2
local c_key_3 = math.random(0x78888,0x9000000)
Key1 = math.random(0x292882399,0x32959505990) 
Key2 = math.random(0x7839900,0x90029293939)
Key3 = math.random(0x567399999,0x9985858484848)
Key4 = math.random(0x28283883,0x599292939393939)
Key5 = math.random(0x47485959,0x78288888888888)
Key6 = math.random(0x1666678866787,0x8886867877888888888)
Key7 = math.random(0x56668888895,0x868778888889)
Key8 = math.random(0x299229299,0x3485940484836)
Key9 = math.random(0x282929299999999,0x80494949494949949499)
Key10 = math.random(0x463739202,0x856363783838888)
Key11 = math.random(0x1111111222,0x99999999999999)
Key12 = math.random(0x1111222233,0x35282940511119)
Key13 = math.random(0x566666666666,0x888888888888888)
Key14 = math.random(0x222222222,0x88888883883928)
Key15 = math.random(0x1263738888,0x82827394949949)
Key16 = math.random(0x12828383838,0x99999999999999)
Key17 = math.random(0x245109837,0x927361937481)
Key18 = math.random(0x33333338848,0x99474749999999)
Key19 = math.random(0x28288383838484848,0x9393949499494949)
Key20 = math.random(0x281,0x9888) Key21 = math.random(0x8287,0x9948)
Key22 = math.random(0x22222222,0x99999999999)
KNTL = math.random(0x28388888,0x937383839838399) 
PPK = math.random(0x287877777,0x47667777777777)
COT = math.random(0x1111,0x972888888) MEK = math.random(0x1737377,0x977474747777)
TOD = math.random(0x99999,0x87299999) SUK = math.random(0x2647777,0x3455555)
KEN = math.random(0x5777776,0x974848888) TOOD = math.random(0x43663666,0x8577488888)
MOD = math.random(0x2474777,0x9885858488)
NGE = math.random(0x988777,0x37778995788)
PXX= 1 * math.random(0x98838888,0x55367373777)
PXX2= 2 * math.random(0x7673777,0x9884888888)
PXXr= 3 * math.random(0x777376666,0x9877474777)
PXXr2= 4 * math.random(0x293666666,0x9858888888888)
PXXX= 5 * math.random(0x111111111,0x8888888888888)
PXXXX = 6 * math.random(0x6393848,0x98499859888)
PXXX2 = 7 * math.random(0x18385778,0x4585899000)
PXXX3 = 8 * math.random(0x87577776,0x9848888888888)
PXXXX2 = 9 * math.random(0x2447577,0x858899979777)
PXXX1 = (PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*PXXXX2+PXXX+PXXX2*PXXX3-PXXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
PXXX2 = (PXX2-PXX+PXXr2*Key2*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*PXXXX2+PXXX+PXXX2*PXXX3-PXXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v1 = (PXXr2*PXXr+PXX2*PXXXX2*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*PXXXX2+PXXX+PXXX2*PXXX3-PXXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v2 = (PXX+PXXr2*Key4*Key2+Key1*Key9*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*PXXXX2+PXXX+PXXX2*PXXX3-PXXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v3 = (PXXX+PXX*Key8*Key15-Key18*PXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v4 = (PXXXX+PXXX*PXXXX+PXXX2*PXXr*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v5 = (PXXX2-PXXr*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v6 = (PXXX3*PXXX2*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v7 = (PXXXX2+PXXX+PXXX2*PXXX3-PXXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_v8 = (PXXX3*PXXX2*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*Key22+Key18-Key2*Key22)
Key_v9 = (PXXXX2+PXXX+PXXX2*PXXX3-PXXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*Key22+Key18-Key2*Key22)
Key_V18 = (PXXXX2+PXXXX*PXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_V18 = (Key1*Key2-Key3*Key4*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*Key8*Key9*Key10+Key11*Key12*Key13-Key14+Key15*Key16-Key17*Key18+Key19-Key20)
Key_V18 = (Key1-Key2-Key3-Key4+Key5-Key6-Key7*Key8*Key9*Key10+Key11*Key12*Key13-Key14+Key15*Key16-Key17*Key18+Key19-Key20*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7)
Key_pull = (PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*Key21*Key20)
Key_mmkv1 = (PXXX3*PXXX2*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*Key21*Key20)
Key_mmkv2 = (PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*PXXXX2+PXXX+PXXX2*PXXX3-PXXXX*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6*Key7)
Key_mmkv3 = (KNTL*PPK+COT+TOD+MOD+TOOD+PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14)
Key_mmkv4 = (KNTL*PPK+COT+TOD+MOD+TOOD+SUK-KEN*NGE-PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14)
Key_mmkv5 = (KNTL*PPK+COT+TOD+MOD+TOOD+SUK-KEN*NGE-MEK*PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14)
Key_mmkv6 = (PXXX3+PXXX2-Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*PXX*PXX2*PXXXX2*Key1*Key5*Key6-Key7+Key8+Key9*Key10*Key11-Key12*Key13-Key14*Key15*Key16+Key17*Key18-Key19*Key20*Key1-Key2-Key3-Key4+Key5-Key6-Key7*Key21*Key20)
Key_Veru = Key_v1 + Key_v2 + Key_v3 + Key_v4 + Key_v5 + Key_v6 + Key_v7 + Key_V18 + Key_V18 - Key_V18 * Key_pull * Key_mmkv1 * Key_mmkv2 * Key_mmkv3 + Key_mmkv4 * Key_mmkv5 + Key_mmkv6 * Key_v8 + Key_v9
for i in ipairs(KYE) do c = ((KYE[i] - Key_Veru  + (PXXX1 + i)  * PXXX2) % 9999) table.insert(KYEEE, c) end
AB = math.random(0x488888888,0x988585999477)
AC = math.random(0x24747777,0x9584877277777)
AD = math.random(0x137474888,0x857484999999999)
AE = math.random(0x35587588,0x5583899999999)
AF = math.random(0x54625555,0x859999999999999)
AG = math.random(0x1648588899,0x7888848585858488)
ABB = math.random(0x7777,0x8995988) ACC = math.random(0x3667777777,0x88888888888888)
ADD = math.random(0x82737772,0x9363677377)
AEE = math.random(0x328374747,0x85747383838388)
AFF = math.random(0x3475757588,0x56292929384747)
AGG = math.random(30747470,608686860)
Arp = math.random(173885892,39178925959959)
ABBB = math.random(107577500,6886582000)
ACCC = math.random(385857000,48585858000)
ADDD = math.random(5072700,6092929200)
AEEE = math.random(70377300,88383838383000)
AFFF = math.random(907373700,1008383837373700)
AGGG = math.random(3737300,684848484800)
local key = {(ACC+ABB*AEE)-ADD,AEE,ADD*1,ACC+AFF,ADD*ACC*ADD*AEE*AFF-ABB}
local Unk = {(AB+AC*AD-AE+AF*AB)-AE,AC-10*AB,AD*2-AB,AE+AD,AF*AD,AB,AG+AF,AD-2,AC+3,AC}
local KY1 = (key[1]+key[3]-key[4])-key[5]  local KY2 = (key[1]-Unk[2]*key[3]*Unk[4])-key[5]
local KY3 = (Unk[2]-Unk[1]*Unk[4]-Unk[3])+Unk[1]
local KY4 = (key[4]+Arp-key[1])*key[2] local Key53 = math.random(19999,585568)
local Key14 = math.random(17877,758900) local key21 = math.random(27977,408900)
local KeySha1 = math.random(84949,949950)
local KeySha2 = math.random(39999,75890)
local Key1 = math.random(19290,19900) local Key2 = math.random(10190,10850)
local Key3 = math.random(12710,13700) local Key4 = math.random(12810,121800)
local Key5 = math.random(13900,16400) local Key6 = math.random(25573,35555)
local getKey = -Key1*Key2-Key3*Key4*Key5*Key2-Key3*Key4*Key5+Key1*Key2-Key3*Key4*Key5*Key2-Key3*Key4*Key5*Key1*Key2-Key3*Key4*Key5*Key2-Key3*Key4*Key5
local Key53 = Key3;local Key14 = Key5;local inv256
local Key53 = 3739449474949484;local Key14 = 9999;local inv256
local Key53 = 3739474949494844;local Key14 = 9998;local inv256
AB = math.random(0x20,0x50) AC = math.random(1500,3000)
AD = math.random(1500,3000) AE = math.random(1500,3000)
AF = math.random(1500,3000) AG = math.random(1500,3000)
Arp = math.random(1500,3000) local key = {(AB+AC*AD-AE+AF*AB)-AE,AC-10*AB,AD*2-AB,AE+AD,AF*AD}
local keyy = {(AB+AC*AD*AB)-AC-1*AB,AD*2-AB,AE-AD,AF*AD-190,AC+AB*12}
local KY3 = {key[4]*key[3]+Arp-keyy[1]} local KY1 = {(key[1]+keyy[3]+key[4]*key[2])-keyy[4]}
local KY2 = {(keyy[5]+key[4]*7)-keyy[2]} local inv256
function b4be5e64b4be5e64() HE = math.random(500,999) for i=1,HE do
x = math.random(0x2990,0x292939) for i=1,899 do
y= math.random(0x2990,0x292939) x=x..y end end end
function ESHA(str)if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 9999 == 1 inv256[M] = inv end;end local K, F = KY1[1] - AG * KY3[1], AB + AG - KY2[1] return (str:gsub('.', function(m)local L = AB + KY2[1] * KY1[1] - 1101010 % KY3[1] local PX = Arp + (keyy[1] * 3) - 110029 local H = (K * PX + L - KY2[1]) / KY3[1];local M = H % 27;local m = m:byte()local c = (m * inv256[M] - (H + M) / 27) % 9999 K = L * F + F + Arp * F - m return ('%02x'):format(c)end)) end
memex = 0 for i = 1, 5 do load(DATA) end kuntul = 0 for i = 1, 10 do load(DATA) end anjer = 0 for i = 1, 20 do load(DATA) end
local XTR = {} local GTV = {} local XGX = {} local RPE = {} local XTG = {} local TEG = {}
for i = 1, 20 do table.insert(XTR, math.random(19, 30))
table.insert(GTV, math.random(30, 80)) table.insert(XGX, math.random(79, 294))
table.insert(RPE, math.random(19, 30)) table.insert(XTG, math.random(30, 80))
table.insert(TEG, math.random(79, 294)) end
local function ENC2(str) return str:gsub('.', function (c)
return string.format('%02x', (string.byte(c)+n_key_n-KEY[20]+KEY[19]-KEY[18]+KEY[17]-KEY[16]+KEY[15]-KEY[14]+KEY[13]-KEY[12]+KEY[11]-KEY[10]+KEY[9]-KEY[8]+KEY[7]-KEY[6]+KEY[5]-KEY[4]+KEY[3]-KEY[2]+KEY[1])%256)
end):gsub(" $", "", 1) end local function ENC(c)
c =  ENC2(c) c = {c:byte(1,-1)} for i in ipairs(c) do
c[i] = c[i] + n_key_n - KEY[13] - KEY[18] + KEY[11] + KEY[7] - KEY[3] + KEY[5] + KEY[9] - KEY[4] - KEY[12] + KEY[8] - KEY[2] - KEY[15] + KEY[16] + KEY[14] + KEY[1] + KEY[6] + (KEY[13] * KEY[10]) - (KEY[17] * KEY[20]) + (KEY[10] * i) * KEY[19]
end AshleyRamirez = table.concat(c, ',')
AshleyRamirez = "N_({" .. AshleyRamirezOfficial .."})"
return AshleyRamirez end local function ENCT2(str)
return str:gsub('.', function (c) return string.format('%02x ', (string.byte(c)-n_key_n+KEY[20]-KEY[19]+KEY[18]-KEY[17]+KEY[16]-KEY[15]+KEY[14]-KEY[13]+KEY[12]-KEY[11]+KEY[10]-KEY[9]+KEY[8]-KEY[7]+KEY[6]-KEY[5]+KEY[4]-KEY[3]+KEY[2]-KEY[1])%256)
end):gsub(" $", "", 1) end local function ENCT(c)
c =  ENCT2(c) c = {c:byte(1,-1)} for i in ipairs(c) do
c[i] = c[i] - n_key_n + KEY[1] + (KEY[20] + KEY[19]) - (KEY[17] + KEY[18]) + (KEY[16] + KEY[15]) - (KEY[13] + KEY[14]) + (KEY[12] + KEY[11]) - (KEY[9] + KEY[10]) + (KEY[8] + KEY[7]) + (KEY[1] + KEY[2]) - (KEY[5] + KEY[6]) + (KEY[3] + KEY[4]) % (((KEY[20] + KEY[19]) * (KEY[4] + KEY[8])) * (KEY[1] + KEY[2]))
end AshleyRamirez = table.concat(c, ',') AshleyRamirez = "X_({" .. AshleyRamirezOfficial .."})"
return AshleyRamirez end local set_enc = math.random(1, 2)
local enc_str = function(c) if set_enc == 1 then
c = ENC(c) elseif set_enc == 2 then c = ENCT(c)
end return c end local enc_func = function(c)
if set_enc == 1 then c = ENCT(c) elseif set_enc == 2 then
c = ENC(c) end return c end local function LESS(c)
NVGB = '\\342' AshleyRamirezMTP = {} for i in ipairs(c) do
NUG = '"' .. NVGB:rep(c[i]) .. '"' table.insert(AshleyRamirezMTP, NUG) end
return table.concat(AshleyRamirezMTP, ",") end
local function LESSING(c) AshleyRamirezMTP = {}
for i in ipairs(c) do NUG = '{' .. c[i] .. '}' table.insert(AshleyRamirezMTP, NUG)
end return table.concat(AshleyRamirezMTP, ",") end
local Key53 = 8186484168865098;local Key14 = 4887;local inv256
function Sha(data) if not inv256 then inv256 = {}
for M = 0, 127 do local inv = -1 repeat inv = inv + 2
until inv * (2*M + 1) % 9999 == 1 inv256[M] = inv end end
if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 9999 == 1 inv256[M] = inv end;end local K, F = Key53, 16384 + Key14 return (data:gsub('.', function(m)local L = K % 274877906944;local H = (K - L) / 274877906944;local M = H % 128;local m = m:byte()local c = (m * inv256[M] - (H - M) / 128) % 9999 K = L * F + H + c + m return ('%02x'):format(c)end))end
KK1 = math.random(1,283)KK2 = math.random(1,283)AB = math.random(1,283) KK3 = math.random(1,283)KEZ = math.random(1,283)KK4 = math.random(1,283)KK5 = math.random(1,283)KK6 = math.random(1,283)Kymy = math.random(1,283)Kyx = math.random(1,283)KK7 = math.random(1,283)KEZ2 = math.random(1,283) KK = math.random(1,283)AC = math.random(1,283) AD = math.random(1,283) KK8 = math.random(1,283)AE = math.random(1,283) AF = math.random(1,283) AG = math.random(1,283) local key = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF} local KY1 = (key[5]+key[2]+key[1]*key[4])-key[1]local KY2 = (key[2]+key[3]*1)-key[4]local KY3 = (key[3]+key[1]*key[2])+key[4]local KY4 = (key[1]+key[2]*key[5]*key[5])+key[1]local KY5 = (key[1]+key[5]-key[3])+key[4]local KY6 = (key[5]+key[2]+key[1]*key[4])-key[1]local KY7 = (key[2]+key[3]*1)-key[4]local KY8 = (key[5]+key[1]*key[2])+key[3]local KY9 = (key[3]+key[4]-key[1]*key[2])+key[5]local KY10 = (key[5]+key[1]-key[2])+key[3]
local ENCAshleyRamirezWK = {} local Key53 = KEZ; local Key14 = KEZ2;
local inv256 function Sha(data) if not inv256 then
inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2
until inv * (2*M + 1) % 9999 == 1 inv256[M] = inv end end
if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 9999 == 1 inv256[M] = inv end;end local K, F = Key53, Kymy + Key14 return (data:gsub('.', function(m)local L = K % Kyx;local H = (K - L) / Kyx;local M = H % 128;local m = m:byte()local c = (m * inv256[M] - (H - M) / 128) % 9999 K = L * F + H + c + m return ('%02x'):format(c)end))end
HUB={KY1,KY2,KY3,KY4,KY5,KY6,KY7,KY8,KY9,KY10,KY9,KY7,KY5,KY4,KY3,KY10,KY5,KY4,KY2,KY3,KY1,KY9}
function ENCAshleyRamirezWKN(c) KEY={} for i in ipairs(c) do
XNXX = (c[i] + HUB[1] + HUB[2] - HUB[6] + HUB[3] - HUB[8] * HUB[4] + HUB[7] - HUB[5] * HUB[10] + HUB[9] * HUB[11] + HUB[12] + HUB[13] + HUB [14] + HUB[15] - HUB[16] - HUB[17] - HUB[18] - HUB[19] - HUB[20]) % 9999
table.insert(KEY, XNXX) end return KEY end ENCAshleyRamirezWKN(HUB)
function ENCAshleyRamirezWKN2(c) KEY2={} for i in ipairs(c) do
XNXX = (c[i] + KEY[1] - (KEY[4] + i) + (KEY[2] + i) - (KEY[6] + KEY[5]) + (KEY[7] + KEY[9]) - KEY[8] + KEY[10] - KEY[14] + KEY[12] - KEY[17] + KEY[11] + KEY[17] + i + KEY[16] * KEY[10]) % 9999
table.insert(KEY2, XNXX) end return KEY2 end
ENCAshleyRamirezWKN2(KEY) function ENCAshleyRamirezWKN3(c) KEY3={} for i in ipairs(c) do
XNXX = (c[i] + KEY2[1] - (KEY2[2] + i) + (KEY2[3] + i) - (KEY2[4] + KEY2[8]) + (KEY2[6] + KEY2[7]) - KEY2[5] + KEY2[9] - KEY2[13] + KEY2[11] - KEY2[15] + KEY2[12] + KEY2[13] + i + KEY2[10] * KEY2[16]) % 9999
table.insert(KEY3, XNXX) end return KEY3 end
ENCAshleyRamirezWKN3(KEY2) function XNX(str) str=Sha(str)
sd = {} gb = {str:byte(0,-1)} res = '' LESS = '\\987'
for i = 1, #gb do gb[i] = (gb[i] - KEY3[1] + KEY3[2] - KEY3[6] + KEY3[3] - KEY3[8] * KEY3[4] + KEY3[7] - KEY3[5] * KEY3[10] + KEY3[9] * KEY3[11] + KEY3[12] + KEY3[13] + KEY3 [14] + KEY3[15] - KEY3[16] - KEY3[17] - KEY3[18] - KEY3[19] - KEY3[20]) % 9999
K=LESS:rep(gb[i]) table.insert(sd, '"'..K..'"') end
return "{"..cCc(sd, ",").."}" end HUB={KY1,KY2,KY3,KY4,KY5,KY6,KY7,KY8,KY9,KY10,KY9,KY7,KY5,KY4,KY3,KY10,KY5,KY4,KY2,KY3,KY1,KY9}
function ENCAshleyRamirezWKN(c) KEY={} for i in ipairs(c) do
XNXX = (c[i] + HUB[1] + HUB[2] - HUB[6] + HUB[3] - HUB[8] * HUB[4] + HUB[7] - HUB[5] * HUB[10] + HUB[9] * HUB[11] + HUB[12] + HUB[13] + HUB [14] + HUB[15] - HUB[16] - HUB[17] - HUB[18] - HUB[19] - HUB[20]) % 9999
table.insert(KEY, XNXX) end return KEY end ENCAshleyRamirezWKN(HUB)
function ENCAshleyRamirezWKN2(c) KEY2={} for i in ipairs(c) do
XNXX = (c[i] + KEY[1] - (KEY[4] + i) + (KEY[2] + i) - (KEY[6] + KEY[5]) + (KEY[7] + KEY[9]) - KEY[8] + KEY[10] - KEY[14] + KEY[12] - KEY[17] + KEY[11] + KEY[17] + i + KEY[16] * KEY[10]) % 9999
table.insert(KEY2, XNXX) end return KEY2 end
ENCAshleyRamirezWKN2(KEY) function ENCAshleyRamirezWKN3(c) KEY3={} for i in ipairs(c) do
XNXX = (c[i] + KEY2[1] - (KEY2[2] + i) + (KEY2[3] + i) - (KEY2[4] + KEY2[8]) + (KEY2[6] + KEY2[7]) - KEY2[5] + KEY2[9] - KEY2[13] + KEY2[11] - KEY2[15] + KEY2[12] + KEY2[13] + i + KEY2[10] * KEY2[16]) % 9999
table.insert(KEY3, XNXX) end return KEY3 end ENCAshleyRamirezWKN3(KEY2)
AB = math.random(1000,20000) ABB = math.random(1000,20000)
ABBB = math.random(1000,20000) AC = math.random(3000,40000)
ACC = math.random(3000,40000) ACCC = math.random(3000,40000)
AD = math.random(5000,60000) ADD = math.random(5000,60000)
ADDD = math.random(5000,60000) AE = math.random(7000,80000)
AEE = math.random(7000,80000) AEEE = math.random(7000,80000)
AF = math.random(9000,100000) AFF = math.random(9000,100000)
AFFF = math.random(9000,100000) AG = math.random(300,600)
AGG = math.random(300,600) AGGG = math.random(300,600)
local keyTM = {(ABBB+ACCC*ADDD)-AEEE,ACCC,ADDD*2,AEEE+ADDD,AFFF}
local KYYY1 = (keyTM[5]+keyTM[3]+keyTM[4]*keyTM[2])-keyTM[4]
local KYYY2 = (keyTM[1]+keyTM[4]*2)-keyTM[2]
local keYy = {(ABB+ACC*ADD)-AEE,ACC,ADD*2,AEE+ADD,AFF}
local KYY1 = (keYy[2]+keYy[4]+keYy[3]*keYy[5])-keYy[3]
local KYY2 = (keYy[2]+keYy[3]*2)-keYy[1]+keYy[5]
local keyy = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF}
local Key1 = (keyy[1]+keyy[3]+keyy[4]*keyy[2])-keyy[4] 
local Key2 = (keyy[5]+keyy[4]*2)-keyy[2] local Key3 = (keyy[3]+keyy[1]*2)-keyy[2]
local Key4 = (keyy[2]+keyy[4]*2)-keyy[2] local Key5 = (keyy[4]+keyy[2]*2)-keyy[2]
local Key6 = (keyy[3]+keyy[2]*2)-keyy[2] function Sha(str)str = str:gsub("\\n", "\n"):gsub("\\t","\t")if not inv256 then inv256 = {} for M = 0, 127 do local inv = -1 repeat inv = inv + 2 until inv * (2*M + 1) % 9999 == 1 inv256[M] = inv end;end local K, F = KYYY1 - AGGG, AGGG - KYYY2 return (str:gsub('.', function(m)local L = K % 19922;local H = (K - L) / 19922;local M = H % 77;local m = m:byte()local c = (m * inv256[M] - (H - M) / 77) % 9999 K = L * F + H + c + m  return ('%02x'):format(c)end)):gsub(" $", "", 1) end
k = math.random(1,20) function EncSTR(str) str = str:gsub("\\n", "\n")
sd = {} gb = {str:byte(1,-1)} res = '' for i = 1, #gb do
gb[i] = (gb[i] - Key1 - (Key2 + i) - Key3 % (Key4 + i) % Key5 - (Key6 + i) * (Key1 + i)) % 9999
end return "{AshleyRamirez = {"..table.concat(gb, ",").."}}" end
function EncSTRR(str) str = str:gsub("\\n", "\n"):gsub("\\t","\t")
c = {str:byte(1, -1)} LESS = "\\"..k.."" sd = {} for i = 1, #c do
c[i] = (c[i] - KYY1 * (KYY2 + i)) % 9999 res = LESS:rep(c[i])
table.insert(sd, '"'..res..'"') end return "{AshleyRamirez={"..table.concat(sd, ",").."}}" end
AB = math.random(1000,20000) AC = math.random(3000,40000)
AD = math.random(5000,60000) AE = math.random(7000,80000)
AF = math.random(9000,100000) AG = math.random(300,600)
ABB = math.random(1000,20000) ACC = math.random(3000,40000)
ADD = math.random(5000,60000) AEE = math.random(7000,80000)
AFF = math.random(9000,100000) AGG = math.random(300,600)
Arp = math.random(100,800) ABBB = math.random(1000,20000)
ACCC = math.random(3000,40000) ADDD = math.random(5000,60000) AEEE = math.random(7000,80000)
AFFF = math.random(9000,100000) AGGG = math.random(300,600)
local key = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF} local KY1 = (key[5]+key[2]+key[1]*key[4])-key[1] local KY2 = (key[2]+key[3]*1)-key[4] local Meow = {}
local keey = {(ABB+ACC*ADD)-AEE,ACC,ADD*2,AEE+ADD,AFF} 
local KYY1 = (keey[3]+keey[5]*keey[4])-keey[1]  local KYY2 = (keey[2]+keey[3]*4)-keey[5]
Keya={} KMM={} for i = 1, 5 do GB = math.random(9, 38)
table.insert(Keya, GB) end for i = 1,5 do Keya[i] = Keya[i] + math.random(81,791)
end for i in ipairs(Keya) do C = (Keya[i] + i - KYY1 - (KYY2 + i) * (KYY1 +i)) % 9999 table.insert(KMM, C) end
Key = {1,1,1,1,1,1,1,1,1,1} Key = {21,1,1,1,1,1,1,1,21,1} Key = {21,16,1,1,1,71,1,1,21,1}
function L33_65734() local L1_85506, L2_85507
L2_85507 = L28_65729 L2_85507 = L2_85507 + L25_65726
L2_85507 = L2_85507 - L30_65731 return (L1_85506:gsub("%x%x", function()
local L0_85508, L1_85509, L2_85510, L3_85511
L1_85509 = L2_85507 L2_85510 = L30_65731
L1_85509 = L1_85509 % L2_85510 L2_85510 = L2_85507
L2_85510 = L2_85510 - L1_85509 L3_85511 = L30_65731
L2_85510 = L2_85510 / L3_85511 L3_85511 = L2_85510 % 27
L0_85508 = tonumber(L0_85508, 16) L2_85507 = L1_85509 * STM3 + L2_85510 + L0_85508 + (L0_85508 + (L2_85510 - L3_85511) / 27) * (2 * L3_85511 + 1) % 9999
return string.char((L0_85508 + (L2_85510 - L3_85511) / 27) * (2 * L3_85511 + 1) % 9999) end)) end
function L33_65734() local L1_85506, L2_85507
L2_85507 = L28_65729 L2_85507 = L2_85507 + L25_65726
L2_85507 = L2_85507 - L30_65731 return (L1_85506:gsub("%x%x", function()
local L0_85508, L1_85509, L2_85510, L3_85511
L1_85509 = L2_85507 L2_85510 = L30_65731
L1_85509 = L1_85509 % L2_85510 L2_85510 = L2_85507
L2_85510 = L2_85510 - L1_85509 L3_85511 = L30_65731
L2_85510 = L2_85510 / L3_85511 L3_85511 = L2_85510 % 27
L0_85508 = tonumber(L0_85508, 16) L2_85507 = L1_85509 * STM3 + L2_85510 + L0_85508 + (L0_85508 + (L2_85510 - L3_85511) / 27) * (2 * L3_85511 + 1) % 9999
return string.char((L0_85508 + (L2_85510 - L3_85511) / 27) * (2 * L3_85511 + 1) % 9999) end)) end
AB = math.random(1,283) AC = math.random(1,283)
AD = math.random(1,283) AE = math.random(1,283)
AF = math.random(1,283) AG = math.random(1,283)
local key = {(AB+AC*AD)-AE,AC,AD*2,AE+AD,AF}local KY1 = (key[5]+key[2]+key[1]*key[4])-key[1]local KY2 = (key[2]+key[3]*1)-key[4]local KY3 = (key[3]+key[1]*key[2])+key[4]local KY4 = (key[1]+key[2]*key[5]*key[5])+key[1]local KY5 = (key[1]+key[5]-key[3])+key[4]local KY6 = (key[5]+key[2]+key[1]*key[4])-key[1]local KY7 = (key[2]+key[3]*1)-key[4]local KY8 = (key[5]+key[1]*key[2])+key[3]local KY9 = (key[3]+key[4]-key[1]*key[2])+key[5]local KY10 = (key[5]+key[1]-key[2])+key[3]
local Key53 = KEY2[2];local Key14 = KEY2[3];local inv256
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
local AshleyRamirezTTTTQ = function(data) data = data.AshleyRamirezTTTT
local K, F = Key53, KEY2[4] + Key14 return (data:gsub('%x%x', function(c) local L = K % KEY2[5] local H = (K - L) / KEY2[5] local M = H % 128 c = tonumber(c, 16) local m = (c + (H - M) / 128) * (2*M + 1) % 9999 K = L * F + H + c + m return string.char(m)end))end
function ENCAshleyRamirezWK(c) c = c.AshleyRamirezTTTT res = '' for i in ipairs(c) do
res = res..string.char((#c[i] + KEY3[5] - KEY3[3] + KEY3[6] - KEY3[3] + KEY3[8] * KEY3[4] - KEY3[7] + KEY3[5] * KEY3[10] - KEY3[9] * KEY3[15] - KEY3[12] - KEY3[13] - KEY3[14] - KEY3[15] + KEY3[16] + KEY3[17] + KEY3[18] + KEY3[19] + KEY3[20]) % 9999) end return res end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local function sha256(msg) local function band(int1, int2, int3, ...) local ret = ((int1%0x00000002>=0x00000001 and int2%0x00000002>=0x00000001 and 0x00000001) or 0)+
((int1%0x00000004>=0x00000002 and int2%0x00000004>=0x00000002 and 0x00000002) or 0)+ ((int1%0x00000008>=0x00000004 and int2%0x00000008>=0x00000004 and 0x00000004) or 0)+
((int1%0x00000010>=0x00000008 and int2%0x00000010>=0x00000008 and 0x00000008) or 0)+ ((int1%0x00000020>=0x00000010 and int2%0x00000020>=0x00000010 and 0x00000010) or 0)+
((int1%0x00000040>=0x00000020 and int2%0x00000040>=0x00000020 and 0x00000020) or 0)+ ((int1%0x00000080>=0x00000040 and int2%0x00000080>=0x00000040 and 0x00000040) or 0)+
((int1%0x00000100>=0x00000080 and int2%0x00000100>=0x00000080 and 0x00000080) or 0)+ ((int1%0x00000200>=0x00000100 and int2%0x00000200>=0x00000100 and 0x00000100) or 0)+
((int1%0x00000400>=0x00000200 and int2%0x00000400>=0x00000200 and 0x00000200) or 0)+ ((int1%0x00000800>=0x00000400 and int2%0x00000800>=0x00000400 and 0x00000400) or 0)+
((int1%0x00001000>=0x00000800 and int2%0x00001000>=0x00000800 and 0x00000800) or 0)+ ((int1%0x00002000>=0x00001000 and int2%0x00002000>=0x00001000 and 0x00001000) or 0)+
((int1%0x00004000>=0x00002000 and int2%0x00004000>=0x00002000 and 0x00002000) or 0)+ ((int1%0x00008000>=0x00004000 and int2%0x00008000>=0x00004000 and 0x00004000) or 0)+
((int1%0x00010000>=0x00008000 and int2%0x00010000>=0x00008000 and 0x00008000) or 0)+ ((int1%0x00020000>=0x00010000 and int2%0x00020000>=0x00010000 and 0x00010000) or 0)+
((int1%0x00040000>=0x00020000 and int2%0x00040000>=0x00020000 and 0x00020000) or 0)+ ((int1%0x00080000>=0x00040000 and int2%0x00080000>=0x00040000 and 0x00040000) or 0)+
((int1%0x00100000>=0x00080000 and int2%0x00100000>=0x00080000 and 0x00080000) or 0)+ ((int1%0x00200000>=0x00100000 and int2%0x00200000>=0x00100000 and 0x00100000) or 0)+
((int1%0x00400000>=0x00200000 and int2%0x00400000>=0x00200000 and 0x00200000) or 0)+ ((int1%0x00800000>=0x00400000 and int2%0x00800000>=0x00400000 and 0x00400000) or 0)+
((int1%0x01000000>=0x00800000 and int2%0x01000000>=0x00800000 and 0x00800000) or 0)+ ((int1%0x02000000>=0x01000000 and int2%0x02000000>=0x01000000 and 0x01000000) or 0)+
((int1%0x04000000>=0x02000000 and int2%0x04000000>=0x02000000 and 0x02000000) or 0)+ ((int1%0x08000000>=0x04000000 and int2%0x08000000>=0x04000000 and 0x04000000) or 0)+
((int1%0x10000000>=0x08000000 and int2%0x10000000>=0x08000000 and 0x08000000) or 0)+ ((int1%0x20000000>=0x10000000 and int2%0x20000000>=0x10000000 and 0x10000000) or 0)+
((int1%0x40000000>=0x20000000 and int2%0x40000000>=0x20000000 and 0x20000000) or 0)+ ((int1%0x80000000>=0x40000000 and int2%0x80000000>=0x40000000 and 0x40000000) or 0)+
((int1>=0x80000000 and int2>=0x80000000 and 0x80000000) or 0) return (int3 and band(ret, int3, ...)) or ret end local function bxor(int1, int2, int3, ...) local ret =
((int1%0x00000002>=0x00000001 ~= (int2%0x00000002>=0x00000001) and 0x00000001) or 0)+ ((int1%0x00000004>=0x00000002 ~= (int2%0x00000004>=0x00000002) and 0x00000002) or 0)+
((int1%0x00000008>=0x00000004 ~= (int2%0x00000008>=0x00000004) and 0x00000004) or 0)+ ((int1%0x00000010>=0x00000008 ~= (int2%0x00000010>=0x00000008) and 0x00000008) or 0)+
((int1%0x00000020>=0x00000010 ~= (int2%0x00000020>=0x00000010) and 0x00000010) or 0)+ ((int1%0x00000040>=0x00000020 ~= (int2%0x00000040>=0x00000020) and 0x00000020) or 0)+
((int1%0x00000080>=0x00000040 ~= (int2%0x00000080>=0x00000040) and 0x00000040) or 0)+ ((int1%0x00000100>=0x00000080 ~= (int2%0x00000100>=0x00000080) and 0x00000080) or 0)+
((int1%0x00000200>=0x00000100 ~= (int2%0x00000200>=0x00000100) and 0x00000100) or 0)+ ((int1%0x00000400>=0x00000200 ~= (int2%0x00000400>=0x00000200) and 0x00000200) or 0)+
((int1%0x00000800>=0x00000400 ~= (int2%0x00000800>=0x00000400) and 0x00000400) or 0)+ ((int1%0x00001000>=0x00000800 ~= (int2%0x00001000>=0x00000800) and 0x00000800) or 0)+
((int1%0x00002000>=0x00001000 ~= (int2%0x00002000>=0x00001000) and 0x00001000) or 0)+ ((int1%0x00004000>=0x00002000 ~= (int2%0x00004000>=0x00002000) and 0x00002000) or 0)+
((int1%0x00008000>=0x00004000 ~= (int2%0x00008000>=0x00004000) and 0x00004000) or 0)+ ((int1%0x00010000>=0x00008000 ~= (int2%0x00010000>=0x00008000) and 0x00008000) or 0)+
((int1%0x00020000>=0x00010000 ~= (int2%0x00020000>=0x00010000) and 0x00010000) or 0)+ ((int1%0x00040000>=0x00020000 ~= (int2%0x00040000>=0x00020000) and 0x00020000) or 0)+
((int1%0x00080000>=0x00040000 ~= (int2%0x00080000>=0x00040000) and 0x00040000) or 0)+ ((int1%0x00100000>=0x00080000 ~= (int2%0x00100000>=0x00080000) and 0x00080000) or 0)+
((int1%0x00200000>=0x00100000 ~= (int2%0x00200000>=0x00100000) and 0x00100000) or 0)+ ((int1%0x00400000>=0x00200000 ~= (int2%0x00400000>=0x00200000) and 0x00200000) or 0)+
((int1%0x00800000>=0x00400000 ~= (int2%0x00800000>=0x00400000) and 0x00400000) or 0)+ ((int1%0x01000000>=0x00800000 ~= (int2%0x01000000>=0x00800000) and 0x00800000) or 0)+
((int1%0x02000000>=0x01000000 ~= (int2%0x02000000>=0x01000000) and 0x01000000) or 0)+ ((int1%0x04000000>=0x02000000 ~= (int2%0x04000000>=0x02000000) and 0x02000000) or 0)+
((int1%0x08000000>=0x04000000 ~= (int2%0x08000000>=0x04000000) and 0x04000000) or 0)+ ((int1%0x10000000>=0x08000000 ~= (int2%0x10000000>=0x08000000) and 0x08000000) or 0)+
((int1%0x20000000>=0x10000000 ~= (int2%0x20000000>=0x10000000) and 0x10000000) or 0)+ ((int1%0x40000000>=0x20000000 ~= (int2%0x40000000>=0x20000000) and 0x20000000) or 0)+
((int1%0x80000000>=0x40000000 ~= (int2%0x80000000>=0x40000000) and 0x40000000) or 0)+ ((int1>=0x80000000 ~= (int2>=0x80000000) and 0x80000000) or 0) return (int3 and bxor(ret, int3, ...)) 
or ret end local function bnot(int) return 4294967295 - int end local function rshift(int, by) local shifted = int / (2 ^ by) return shifted - shifted % 1 end local function rrotate(int, by) local shifted = int / (2 ^ by) local fraction = shifted % 1
return (shifted - fraction) + fraction * (2 ^ 32) end local k = {0x428a2f98, 0x71374491, 0xb5c0fbcf, 0xe9b5dba5,0x3956c25b, 0x59f111f1, 0x923f82a4, 0xab1c5ed5,0xd807aa98, 0x12835b01, 0x243185be, 0x550c7dc3,0x72be5d74, 0x80deb1fe, 0x9bdc06a7, 0xc19bf174,0xe49b69c1, 0xefbe4786, 0x0fc19dc6, 0x240ca1cc,0x2de92c6f, 0x4a7484aa, 0x5cb0a9dc, 0x76f988da,0x983e5152, 0xa831c66d, 0xb00327c8, 0xbf597fc7,0xc6e00bf3, 0xd5a79147, 0x06ca6351, 0x14292967,0x27b70a85, 0x2e1b2138, 0x4d2c6dfc, 0x53380d13,0x650a7354, 0x766a0abb, 0x81c2c92e, 0x92722c85,0xa2bfe8a1, 0xa81a664b, 0xc24b8b70, 0xc76c51a3,0xd192e819, 0xd6990624, 0xf40e3585, 0x106aa070,0x19a4c116, 0x1e376c08, 0x2748774c, 0x34b0bcb5,0x391c0cb3, 0x4ed8aa4a, 0x5b9cca4f, 0x682e6ff3,0x748f82ee, 0x78a5636f, 0x84c87814, 0x8cc70208,0x90befffa, 0xa4506ceb, 0xbef9a3f7, 0xc67178f2,}
local function str2hexa(s) local h = string.gsub(s, ".", function(c)return string.format("%02x", string.byte(c))end) return h end local function num2s(l, n)local s = "" for i = 1, n do local rem = l % 9999s = string.char(rem) .. s l = (l - rem) / 256
end return s end local function s232num(s, i) local n = 0 for i = i, i + 3 do n = n*256 + string.byte(s, i) end return n end local function preproc(msg, len) local extra = 64 - ((len + 1 + 8) % 64) len = num2s(8 * len, 8)
msg = msg .. "\128" .. string.rep("\0", extra) .. len return msg end local function initH256(H) H[1] = 0x6a09e667 H[2] = 0xbb67ae85 H[3] = 0x3c6ef372 H[4] = 0xa54ff53a H[5] = 0x510e527f H[6] = 0x9b05688c H[7] = 0x1f83d9ab H[8] = 0x5be0cd19
return H end local function digestblock(msg, i, H) local w = {} for j = 1, 16 do w[j] = s232num(msg, i + (j - 1) * 4) end for j = 17, 64 do local v = w[j - 15] local s0 = bxor(rrotate(v, 7), rrotate(v, 18), rshift(v, 3)) v = w[j - 2] local s1 = bxor(rrotate(v, 17), rrotate(v, 19), rshift(v, 10))
w[j] = w[j - 16] + s0 + w[j - 7] + s1 end local a, b, c, d, e, f, g, h = H[1], H[2], H[3], H[4], H[5], H[6], H[7], H[8] for i = 1, 64 do local s0 = bxor(rrotate(a, 2), rrotate(a, 13), rrotate(a, 22)) local maj = bxor(band(a, b), band(a, c), band(b, c))
local t2 = s0 + maj local s1 = bxor(rrotate(e, 6), rrotate(e, 11), rrotate(e, 25)) local ch = bxor (band(e, f), band(bnot(e), g)) local t1 = h + s1 + ch + k[i] + w[i] h, g, f, e, d, c, b, a = g, f, e, d + t1, c, b, a, t1 + t2
end H[1] = band(H[1], a) H[2] = band(H[2], b) H[3] = band(H[3], c) H[4] = band(H[4], d) H[5] = band(H[5], e) H[6] = band(H[6], f) H[7] = band(H[7], g) H[8] = band(H[8], h) end msg = preproc(msg, #msg) local H = initH256({})
for i = 1, #msg, 64 do digestblock(msg, i, H) end return str2hexa(num2s(H[1], 4) .. num2s(H[2], 4) .. num2s(H[3], 4) .. num2s(H[4], 4) .. num2s(H[5], 4) .. num2s(H[6], 4) .. num2s(H[7], 4) .. num2s(H[8], 4)) end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local b = "#@&?!:;_~`|/<>*-abcdefghijklmnopqrstuvwxyewekABCDEFGHIJKLMNOPQRSTUVWXYewekKONTOLLLLLOSEMUANGENTOTTTT0123456789+/"
function SHA(data) for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end; data = string.gsub(data, '[^'..b..'=]', '') for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
return (data:gsub('.', function(x) if (x == '=') then return '' end for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end; local r,f='',(b:find(x)-1) for i=6,1,-1 do r=r..(f%2^i-f%2^(i-1)>0 and '1' or '0') end
for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end; return r; end):gsub('%d%d%d?%d?%d?%d?%d?%d?', function(x) if (#x ~= 8) then return '' end for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end;
local c=0 for i=1,8 do c=c+(x:sub(i,i)=='1' and 2^(8-i) or 0) end for x=1,0 do;local j={}if j.x~=nil then j.x=j.x()end;end; return string.char(c) end)) end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function bigLasm(source) pattern = "" str = "" m = {}
mm = {}nconstant ={} shit = tostring(Instruction[1])
shit = shit:gsub("%w+", function (cc) m[#m+1] = string.format("%x",cc)
if string.len(m[#m])== 1 then m[#m]="0"..m[#m]
end end) for x = 1, #m do str = str .. m[x] end
number = hexToNum(str) str = escapeOpcode(str)
pattern = formatPattern(dzsh(str),1,number*4)
areShit = tostring(pattern.."(....)") constantNumber = source:match(areShit)
constant[1] = table.concat({constantNumber:byte(1, -1)}, ",")
shut = tostring(constant[1]) shit = shut:gsub("%w+", function(cc)
mm[#mm+1] = string.format("%x",cc) if string.len(mm[#mm])== 1 then
mm[#mm]="0"..mm[#mm] end end) mmx = '' for x = 1, #mm do
mmx = mmx .. mm[x] end mmx = numToHex(tostring(hexToNum(mmx) + 1))
source = source:gsub(escapeOpcode(constantNumber), escapeOpcode(dzsh(mmx) .. randomCode(math.random(7500,9500)),true)..dzsh("00"))
numberOfInstructions = 3 randomInstructions, numberOfInstructions = zjmRand(math.random(30,80),numberOfInstructions), numToHex(numberOfInstructions)
source = source:gsub(escapeOpcode(dzsh("05000000250000000800008006004000")), escapeOpcode(dzsh(numberOfInstructions)..dzsh("25000000")..randomInstructions,true))
return source end function antiLasm(source)
for i = 1, #func do indicator = dzsh(func[i]["LineStarted"] ..func[i]["LineEnded"] .. func[i]["Parameter"] .. func[i]["isVararg"] .. func[i]["maxStack"])
indicator = escapeOpcode(indicator) replacement = dzsh(numToHex(math.random(2447483649, 3294967296)) .. numToHex(math.random(2447483649, 3294967296))) .. dzsh("FA01FA")
replacement = escapeOpcode(replacement, true)
ins = string.match(source, indicator .. "[^\20-\7e][^\20-\7e][^\20-\7e][^\20-\7e]") -- 提取后一个空白Byte (Number of Instructions)
if Instruction[2]==nil then if ins ~= nil then ins = string.sub(ins, string.len(ins) - 3, string.len(ins))
end Instruction[#Instruction + 1] = table.concat({ins:byte(1, -1)}, ",") end
source = source:gsub(indicator, replacement) end return source end
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local GTBL = {} local TBNUB = {} function TB(str) sd = {}
gb = {str:byte(1,-1)} res = '' LESS = '\\210' for i = 1, #gb do gb[i] = (gb[i] + TBNUB[1] - TBNUB[2] * TBNUB[3] * TBNUB[4] - TBNUB[5] * TBNUB[6] - TBNUB[7] * TBNUB[8] - TBNUB[9] + TBNUB[10] * i) % 9999
res = LESS:rep(gb[i]) table.insert(sd, '"'..res..'"') end
return "{"..table.concat(sd, ",").."}" end eek = 1
for i = 1, 10 do gay = math.random(1, 93) table.insert(TBNUB, gay) end
function JomKey() sd = {} res = '' LESS = '\\210' for i = 1, #TBNUB do
res = LESS:rep(TBNUB[i]) table.insert(sd, '"'..res..'"') end keyAshleyRamirez = "{"..table.concat(sd, ",").."}"
table.insert(GTBL, keyAshleyRamirez) end local GTBL = {} local TBNUB = {}
function TB(str) sd = {} gb = {str:byte(1,-1)} res = '' LESS = '\\000'
for i = 1, #gb do gb[i] = (gb[i] + TBNUB[1] - TBNUB[2] * TBNUB[3] * TBNUB[4] - TBNUB[5] * TBNUB[6] - TBNUB[7] * TBNUB[8] - TBNUB[9] + TBNUB[10] * i) % 9999
res = LESS:rep(gb[i]) table.insert(sd, '"'..res..'"') end
return "{"..table.concat(sd, ",").."}" end eek = 1
for i = 1, 10 do gay = math.random(1, 93) table.insert(TBNUB, gay) end
function JomKey() sd = {} res = '' LESS = '\\000' for i = 1, #TBNUB do
res = LESS:rep(TBNUB[i]) table.insert(sd, '"'..res..'"') end
keyAshleyRamirez = "{"..table.concat(sd, ",").."}" table.insert(GTBL, keyAshleyRamirez) end
local GTBL = {} local TBNUB = {} function TB(str) sd = {}
gb = {str:byte(1,-1)} res = '' LESS = '\\95' for i = 1, #gb do gb[i] = (gb[i] + TBNUB[1] - TBNUB[2] * TBNUB[3] * TBNUB[4] - TBNUB[5] * TBNUB[6] - TBNUB[7] * TBNUB[8] - TBNUB[9] + TBNUB[10] * i) % 9999
res = LESS:rep(gb[i]) table.insert(sd, '"'..res..'"') end
return "{"..table.concat(sd, ",").."}" end eek = 1
for i = 1, 10 do gay = math.random(1, 93) table.insert(TBNUB, gay) end
function JomKey() sd = {} res = '' LESS = '\\95' for i = 1, #TBNUB do
res = LESS:rep(TBNUB[i]) table.insert(sd, '"'..res..'"') end
keyAshleyRamirez = "{"..table.concat(sd, ",").."}" table.insert(GTBL, keyAshleyRamirez) end
DATA = DATA:gsub("gg.searchNumber","\ngg.toast('⚠️ PROTECT BY AshleyRamirezOfficial ⚠️')\ngg.searchNumber\n")
DATA = DATA:gsub("gg.clearResults","\ngg.toast('⚠️ PROTECT BY AshleyRamirezOfficial ⚠️')\ngg.clearResults\n")
DATA = DATA:gsub("gg.editAll","\ngg.toast('⚠️ PROTECT BY AshleyRamirezOfficial ⚠️')\ngg.editAll\n")
DATA = DATA:gsub("os.remove","\ngg.toast('⚠️ PROTECT BY AshleyRamirezOfficial ⚠️')\nos.remove\n")
DATA = DATA:gsub("gg.setVisible","\ngg.toast('⚠️ PROTECT BY AshleyRamirezOfficial ⚠️')\ngg.setVisible\n")
DATA = DATA:gsub("gg.setRanges","\ngg.toast('⚠️ PROTECT BY AshleyRamirezOfficial ⚠️')\ngg.setRanges\n")
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
local HIDE = {} local keys = {} function gb(c) c = #c return c end tiger ={} tiger.stringg = string
cnx = tiger.stringg.char function seniors(c) res = '' for i = 1, gb(c) do res = res..cnx((gb(c[i]) + gb(keys[1][1]) + (gb(keys[1][2]) + i) * (gb(keys[1][1]) + i)) % 9999)
end return res end function enAshleyRamirezptbyAshleyRamirez(c) res = '' for i = 1, gb(c) do res = res..cnx((gb(c[i]) + gb(keys[1][1]) + (gb(keys[1][2]) + i) * (gb(keys[1][1]) + i)) % 9999) end return res end
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function zjm_base(cmz) local zjm if cmz == 1 then
zjm = dzsh("01000000") elseif cmz == 2 then
zjm = dzsh("01") .. string.char(math.random(0, 33)) .. dzsh("0000") elseif cmz == 3 then
zjm = dzsh("ADF09F87") elseif cmz == 4 then
zjm = string.char(math.random(4487, 6588483)) .. dzsh("F09F87") elseif cmz == 5 then
zjm = string.char(math.random(148811, 1247747477)) .. dzsh("F09F87") elseif cmz == 6 then
zjm = string.char(math.random(17473, 1888891)) .. dzsh("F09F87") elseif cmz == 7 then
zjm = string.char(math.random(239, 255)) .. dzsh("F09F87") elseif cmz == 8 then
zjm = dzsh("A7") .. string.char(math.random(0, 33), math.random(0, 33), math.random(0, 33)) elseif cmz == 9 then
zjm = dzsh("ACF09F87") elseif cmz == 10 then
zjm = string.char(math.random(0, 255)) .. dzsh("000000") elseif cmz == 11 then
zjm = dzsh("41010000") elseif cmz == 12 then
zjm = dzsh("01000000") elseif cmz == 13 then
zjm = string.char(math.random(47, 63)) .. dzsh("000001") elseif cmz == 14 then
zjm = string.char(math.random(111, 127)) .. dzsh("000001") elseif cmz == 15 then
zjm = string.char(math.random(173, 191)) .. dzsh("000001") elseif cmz == 16 then
zjm = string.char(math.random(239, 255)) .. dzsh("000001") elseif cmz == 17 then
zjm = dzsh("C1000000") elseif cmz == 18 then
zjm = dzsh("81000000") elseif cmz == 19 then
zjm = dzsh("41000000") else zjm = string.char(math.random(133, 255), math.random(0, 33), math.random(97, 122), math.random(133, 255)) -- 随机
end return zjm end function xZiJie(counl) local zjmre = string.char() for i = 1, counl do
zjmre = zjmre .. zjm_base(math.random(1, 20)) end return zjmre end
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function zjmRand(sz,number) local a = "" local number = number
local inittime = os.clock() local max, min = 58, 8
zjms = {} for s = max, min, -1 do str = string.dump(load(randtext(s)), true)
bytstr = str:sub(34, 34 + s * 4 - 1) zjms[s] =bytstr:sub(0, 4) .. dzsh("1F008000") .. xZiJie(s - 2) end
for i = 1 , sz do n = math.random(8,58) a = a .. zjms[n]
number = number + n end return a, number end
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
function XXXX() 
  local SSS = function(code) local res = ""   for i in ipairs(code) do res = res..string.char(code[i]) end  return res end if tostring(_ENV.gg):match(SSS({229,141,151,228,184,131,233,152,178,230,139,166,230,136,170,49,46,48,229,138,160,229,175,134})) then while(true) do   gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165)) 
     os.exit() end else   for k in(tostring(_ENV):gmatch(SSS({229,141,151,228,184,131,233,152,178,230,139,166,230,136,170,49,46,48,229,138,160,229,175,134}))) do     if k ~= gg.getFile() then while(true) do       gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165)) 
       os.exit() end  end   end end  if debug.traceback == nil or gg.getFile == nil then while(true) do  gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165)) 
   os.exit() end end for j in tostring(debug.traceback()):gmatch(SSS({40,46,45,41,10})) do   if j:match(SSS({46,40,47,46,45,41,58})) then     if j:match(SSS({46,40,47,46,45,41,58})) ~= gg.getFile() then while(true) do       gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165)) 
       os.exit() end     end   end end local f = io.open(gg.FILES_DIR:match("^(.*/)([^/]*)$").."shared_prefs/"..gg.PACKAGE.."_preferences.xml", "r") if not f then while(true) do   gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165)) 
   os.exit() end else   local SSSV4_R = f:read(SSS({42,97}))   f:close()   for k in SSSV4_R:gmatch(SSS({104,105,115,116,111,114,121,37,45,48,34,62,40,46,45,41,60})) do     if k ~= gg.getFile() then while(true) do       gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165)) 
       os.exit() end     end   end end end
function XXXX() if 0<#string.sub(debug.traceback(),string.find(debug.traceback(),"chunk")+7,string.find(debug.traceback(),"%[")- 21)then while true do gg.alert(string.char())  os.exit()gg.processKill()end end  iiu=1 while debug.getinfo(iiu, "S") and string.format("%s", debug.getinfo(iiu, "S").short_src) ~= gg.getFile() do gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165))   os.exit() end while string.format("%s", debug.getinfo(print, "S").short_src) ~= "print" do gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165))    os.exit() end while string.format("%s", debug.getinfo(gg.getFile, "S").short_src) ~= "getFile" do gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165))   os.exit() end while string.format("%s", debug.getinfo(debug.traceback, "S").short_src) ~= "wrap" do gg.alert(string.char(240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,202,128,202,143,225,180,152,225,180,155,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,225,180,128,225,180,133,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,202,159,225,180,143,201,162,32,240,159,148,165,10,240,159,148,165,32,225,180,133,225,180,143,201,180,225,180,155,32,225,180,155,202,128,202,143,32,225,180,155,225,180,143,32,225,180,133,225,180,135,225,180,132,225,180,155,202,143,225,180,152,225,180,155,32,240,159,148,165))   os.exit() end end
if string.gsub(string.gsub(io.open("/data/user/0/"..string.match(gg.EXT_FILES_DIR,"data/(.-)/").."/shared_prefs/"..string.match(gg.EXT_FILES_DIR,"data/(.-)/").."_preferences.xml"):read("*a") , "-", "") , tostring(string.char(34)), ""):match("history-sticked") ~=nil then  gg.alert(string.char(229,176,143,233,179,132,233,177,188,239,188,154,232,167,163,229,175,134,229,164,177,232,180,165)) 
   end

function Enc(_AA_)
  do
    for _BB_ = 1, #_AA_ do
      bb = string.byte((string.sub(_AA_, _BB_, _BB_)))
      if aaa == nil then
        aaa = 1
        result = tonumber(bb)
      else
        result = result .. "," .. tonumber(bb)
      end
    end return result
  end
end
function EncPMD(_AA_)
  do
    for _BB_ = 1, #_AA_ do
      bb = string.byte((string.sub(_AA_, _BB_, _BB_)))
      if aaa == nil then
        aaa = 1
        result = tonumber(bb)
      else
        result = result .. "," .. tonumber(bb)
      end
    end return "load(string.char(table.unpack({"..result.."})))()"
  end
end
function RandomLetter(Num)
  MSWKPRO = ""
  for x = 1, Num do
    X = math.random(65, 91)
    if X == 91 then
      MSWKPRO = MSWKPRO .. string.char(X + 4)
    else
      MSWKPRO = MSWKPRO .. string.char(X)
    end
  end
  return MSWKPRO
end

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
while (nil)do;local o={{-nil,{nil%- nil,{-nil%nil,{nil%nil%- nil,{""..AshleyRamirez..""}},{AshleyRamirez},}},{{" �� � � �� ☠���� ������☠� � � �� ��� � � �� ☠���� ������AshleyRamirez � � � �� ��� � ☠� �� AshleyRamirez ���� ����☠2��� � � �� ���ʃ��  �  D  @�؁c  � A �A☠� �� B��  A����  � A �A� �� B�� � A���� A@�   ݀   �    K  �����X� ☠��� �\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠\n"},o.uo,{{"\n☠AshleyRamirezOfficial?? AshleyRamirezOfficial ?? YOU NOOB☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠AshleyRamirezOfficial ?? AshleyRamirezOfficial AshleyRamirezOfficial☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n �� � � ☠�� ���� �������☠ � � �� ��� � � �� ���� ����☠��� � � �� ��� � � �� ���☠� ������� � � �� ���ʃ��  �  D  @�؁c  � A AshleyRamirez �A� �� B��  A���AshleyRamirez �  � A �A� �☠� B�� � A���� A@�   ݀   �    K  ☠���☠ P R O T E C T I O N ☠\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n��X� ��☠�� �\n           �� � � �� ���� ������� � � �� �☠�� � � �� ���� ������� � � �� ��� ☠� � �� ���� �������AshleyRamirez  � � �� ���ʃ��  �  D  @�؁c  � A �A☠� �� B��  A����  � A �A� �� B�� � A���� A@�   ݀   �    K  ��☠���X� ��� �\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠AshleyRamirezOfficial ??  P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n"},p.p,{{"\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠🇷 AshleyRamirez 🇷?? AshleyRamirez☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By 𝙰𝚂??𝙻𝙴𝚈𝚁𝙰𝙼𝙸𝚁𝙴𝚉🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By 𝙰𝚂𝙷𝙻𝙴????𝙰𝙼𝙸𝚁𝙴𝚉🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n �� � � �� ��??�� ������� � � �� ��� � � �� �☠��� ������� � � �� ��� ☠� � �� ���� ������� � � �� AshleyRamirez ���ʃ��  �  D  @�؁c  � A �A☠� �� B��  A����  � A �A� �� B�� � A���� A@�   ݀   �    K  �����X� �☠�� �\n                         A N T I B A N NOOB"},fq.qo.o,{{"\t �� � � ☠�� ���� ������� � � �� ��� � ☠� �� ☠ P R O T E C T I O N ☠\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠���� ������� � � �� ��☠� � � �� ���� ������� � � �☠� ���ʃ��  �  D  @�؁c  � A �A� �� B��  A����  � A �A� �� B�� � A���☠� A@�   ݀   �    K  ��\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N  ??☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n�\n\n??☠ P R O T E C T I O N ☠☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n          ◁━━━━━━◈✙◈━━━━━▷\n[🛡️ ENAshleyRamirezPT TOOL BY RAR AshleyRamirez🛡️]\n         ✭  ♔〘ᏒᎪᏒ ᎬsᏢᎾᏒᏆ™〙♔  ✭\n        ◁━━━━━━◈✙◈━━━━━▷\n�\t\n"},p.p,{{"\t �� � � �� �☠��� �����☠☠�� � � �� ��� � � �� ���� ������� � � ☠�� ��� \n☠ P R O T E C T I O N ☠---[🛡Encoded By 𝙰𝚂𝙷𝙻𝙴𝚈🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By 𝙰𝚂𝙷𝙻𝙴𝚈🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By 𝙰𝚂𝙷𝙻𝙴𝚈🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By 𝙰𝚂𝙷𝙻𝙴𝚈🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠AshleyRamirez AshleyRamirez 🇨 🇮  🇱  🇾  🇾 ??☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n"},q.q{o}.uo,{{"\n�\n🛡Encoded By AshleyRamirez🛡]\n\n �� � � �� ���� ������� � � �� ��� � � �� ���� ������� � � �� ��� � � �� ���� ������� � � �� ���ʃ��  �  D  @�؁c  � A �A� �AshleyRamirez � B��  A����  � A �A� �� B�� � A���� A@�   ݀   �    K  �����X� �AshleyRamirez �� �\n"},p.p,{{"\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠🇷 ?? AshleyRamirez 🇷 AshleyRamirez 🇨 🇮  🇱  🇾 🇹☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[??Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n\n               ��A�C�L�G�NTENG�\t �� � � �� ���� ������� � � �� ��� � � �� ���� AshleyRamirez ������ � � �� ��� � � �� ���� ������� � � �� ���ʃ��  �  D  @�؁c  AshleyRamirez  A �A� �� B��  A����  � A �A� �� B�� � A���� A@�   ݀   �    K  �����X� ��� �\n           �\t\n�\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠?? AshleyRamirez 🇷 AshleyRamirez AshleyRamirez☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[??Encoded By AshleyRamirez🛡]\n\n??☠ P R O T E C T I O N ☠☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n\t �� � � �� ���� ������� � � �� ��� � � �� ���� �����AshleyRamirez � � � �� ��� � � �� ���� ������� � AshleyRamirez  �� ���ʃ��  �  D  @�؁c  � A �A� �� B��  A����  � A �A� �� B�� � A���AshleyRamirez  A@�   ݀   �    K  �����X� ��� �\n"},q.qo.o,{{"\n �� � � �� ���� ������� � � �� ��� � � �� ���� ������� � � �� ��� � � �� ���� ������� � � �� ���ʃ�AshleyRamirez   �  D  @�؁c  � A �A� �� B��  A����  � A �A� �� B�� � A���� A@�   ݀   �    K  �����X� ��� �\t\n�\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠AshleyRamirez ?? AshleyRamirez 🇨  🇮 🇱 🇾 🇹☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n\t \n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n�� ��� � � �� ���� �����AshleyRamirez � � � �� \n\n\t\n"},p.p,{{"\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n�AshleyRamirez�X�RAR�\t �� � � �� ���� ������� � � AshleyRamirez �� ��� � � �� ���� ������� � � �� ��� � � �� ���� ������� � � �� ���ʃ☠ P R O T E C T I O N ☠\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠��  �  D  @�؁c  � A �A� �� B�� \n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠A����  � A �A� �� B�� � A���� A@�   ݀   �    K  �����X� ��� �\n"},q.q}}}}}}}}}}} local p={o.o,{{"\n"},M,A,T,I,C,H,E,L,O,G,{{"\n �� � � �� ���� ������� � � �� ��� � � �� ���� ������� � � �� �\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠�� � � �� AshleyRamirez ��� ������� � � �� ���ʃ��  �  D  @�؁c  � A �A� �� B��  A����  � A �A� �� B�� � A�AshleyRamirez �� A@�   ݀   �    K  �����X� ��� �"},p.p,q.qo.o,{p.p,{q.q.o,{p.s{"\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠AshleyRamirez ?? AshleyRamirez☠---[🛡Encoded By AshleyRamirez🛡]\n\n??🇷 ?? 🇷 AshleyRamirez AshleyRamirez☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠🇷 ?? 🇷 AshleyRamirez AshleyRamirez☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirez🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n☠ P R O T E C T I O N ☠---[🛡Encoded By AshleyRamirezOfficial🛡]\n\n��☠�  � A �A� �� B�� � A�AshleyRamirezOfficial �� A@�   ݀   �    K  ☠����☠�X� ��� �\n"},p,{q.q}}}}}}} local q={o.o,p.p,q.qo.uo,p.pp,q.qo.o,p.p,q.qo.o,p.p,q.qi}local o={o.uo,p.p,q.qo.o,p.rp,q.qo.uo,p.p,q.qo.o,p.p,q.q} local p={M,A,T,I,C,H,E,L,O} local q={o.o,p.p,q.qo.uo,p.p,q,qi,p.p,q.qo.o,p.p,q.qi}if (o.o)then if (o.o.o)then if (o.o.o.o) then if (o.o.o.o.o) then if (p.p) then if (p.p.p) then if (p.p.p.p) then if (q.q) then if (q.q.q) then if (q.q.q.q) then;o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q))))))o.o=(o.o(o)) o.o=(o.o(o.o.o(o.o(o)))) p.p=(p.p(p)) p.p=(p.p(p.p.p(p.p.p.p(p.p.p(p.p(p.p)))))) q.q = (q.q(q.q.q(q.q.q.q(q.q.q(q.q(q.q)))))) local r={o.o,p.p,q.qo.o,p.p,q.q} r.r=r[1]..r[2]..r[3] r.i= r.r(r.r(r.r(r.r(r.r(r.r(r.r)))))) end;end;end;end;end;end;end;end;end;end;end
if(nil)then if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end if true then return end end
local func={['collectgarbage']=collectgarbage,['tostring']=tostring,['load']=load,['concat']=table.concat,['remove']=table.remove,['sort']=table.sort,['pack']=table.pack,['move']=table.move,['insert']=table.insert,['unpack']=table.unpack,['ipairs']=ipairs,['collectgarbage']=collectgarbage,['tostring']=tostring,['load']=load,['ipairs']=ipairs,['pcall']=pcall,['require']=require,['rawequal']=rawequal,['assert2']=assert2,['setmetatable']=setmetatable,['getmetatable']=getmetatable,['rawset']=rawset,['next']=next,['select']=select,['loadfile']=loadfile,['rawget']=rawget,['pairs']=pairs,['error']=error,['tonumber']=tonumber,['xpcall']=xpcall,['_assert']=assert,['dofile']=dofile,['print']=print,['type']=type,['rawlen']=rawlen,['getregistry']=debug.getregistry,['getuservalue']=debug.getuservalue,['setuservalue']=debug.setuservalue,['getupvalue']=debug.getupvalue,['getinfo']=debug.getinfo,['getlocal']=debug.getlocal,['setlocal']=debug.setlocal,['setupvalue']=debug.setupvalue,['traceback']=debug.traceback,['getmetatable']=debug.getmetatable,['setmetatable']=debug.setmetatable,['debug']=debug.debug,['upvaluejoin']=debug.upvaluejoin,['getxnxxxxxx']=debug.getxnxxxxxx,['setxnxxxxxx']=debug.setxnxxxxxx,['upvalueid']=debug.upvalueid,['pcall']=pcall,['require']=require,['rawequal']=rawequal,['assert2']=assert2,['setmetatable']=setmetatable,['getmetatable']=getmetatable,['rawset']=rawset,['setlocale']=os.setlocale,['clock']=os.clock,['tmpname']=os.tmpname,['getenv']=os.getenv,['execute']=os.execute,['difftime']=os.difftime,['rename']=os.rename,['exit']=os.exit,['remove']=os.remove,['time']=os.time,['date']=os.date,['popen']=io.popen,['lines']=io.lines,['write']=io.write,['tmpfile']=io.tmpfile,['open']=io.open,['close']=io.close,['input']=io.input,['read']=io.read,['output']=io.output,['flush']=io.flush,['type']=io.type,['loadlib']=package.loadlib,['searchpath']=package.searchpath,['rshift']=bit32.rshift,['bnot']=bit32.bnot,['lshift']=bit32.lshift,['bxor']=bit32.bxor,['btest']=bit32.btest,['extract']=bit32.extract,['lrotate']=bit32.lrotate,['rrotate']=bit32.rrotate,['band']=bit32.band,['replace']=bit32.replace,['bor']=bit32.bor,['arshift']=bit32.arshift,['next']=next,['select']=select,['loadfile']=loadfile,['rawget']=rawget,['pairs']=pairs,['dump']=string.dump,['reverse']=string.reverse,['char_']=string.char,['unpack']=string.unpack,['match']=string.match,['gsub']=string.gsub,['find']=string.find,['pack']=string.pack,['gmatch']=string.gmatch,['format']=string.format,['packsize']=string.packsize,['lower']=string.lower,['upper']=string.upper,['rep']=string.rep,['sub']=string.sub,['byte_']=string.byte,['len']=string.len,['error']=error,['tonumber']=tonumber,['sqrt']=math.sqrt,['atan2']=math.atan2,['ceil']=math.ceil,['tanh']=math.tanh,['rad']=math.rad,['abs']=math.abs,['sinh']=math.sinh,['atan2']=math.atan,['fmod']=math.fmod,['random']=math.random,['randomseed']=math.randomseed,['max']=math.max,['modf']=math.modf,['ldexp']=math.ldexp,['exp']=math.exp,['deg']=math.deg,['cosh']=math.cosh,['ult']=math.ult,['log']=math.log,['tointeger']=math.tointeger,['frexp']=math.frexp,['asin']=math.asin,['tan']=math.tan,['floor']=math.floor,['pow']=math.pow,['acos']=math.acos,['cos']=math.cos,['type']=math.type,['sin']=math.sin,['min']=math.min,['xpcall']=xpcall,['_assert']=assert,['dofile']=dofile,['print']=print,['type']=type,['rawlen']=rawlen}
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local DATA = io.input(g.last):read('*a')

Mk = math.random(2,63)
KY = {}
for i = 1,10 do
S = Mk + math.random(2,53)
table.insert(KY, S)
end
function MISWAK05(c)
KEY ={}
for i in ipairs(c) do
XNXX = (c[i] + KY[1] + KY[2] * KY[3] + KY[4] * KY[5]) % 256
table.insert(KEY, XNXX)
end
return KEY
end
MISWAK05(KY)
local KAY = (KEY[1]+KEY[2]*KEY[3])*KEY[5]
local KAY2 = (KEY[1]+KEY[5]-KEY[6]*KEY[7])+KEY[8]

function enc(str)
str = str:gsub("\\n", "\n"):gsub("\\t","\t")
gb = {str:byte(0,-1)}
res = ''
LESS = '\\000'
for i = 1, #gb do
gb[i] = (gb[i] - KAY - (KAY2 + i) * (KAY + i)) % 256
end
return "{"..table.concat(gb, ",").."}"
end
function encodegg(A0_67)
	return 'gg[MSWKK({sc = "' .. Sha(A0_67) .. '"})]('
end
function encodeggg(A0_67)
	return '' .. enc(A0_67) .. ')'
end
function encodeos(A0_68)
	return 'os[MSWK(\n' .. enc(A0_68) .. '\n)]('
end
function encodestr(A0_69)
	return 'string[MSWK(\n' .. enc(A0_69) .. '\n)]('
end
function encvalues(A0_70)
	return 'MSWK(\n' .. enc(A0_70) .. '\n)'
end

lasm = 'B = "MISWAK5"\n'
lasm = lasm:rep(1000)
MSWK =
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
local B
..lasm..
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
while(nil)do;i = {nil % nil};for i in ipairs(i) do i = {{nil % nil}, {nil % nil}} i.i = _ENV[{(nil % nil)}] end;end
local MSWKKey = {..table.concat(KY, ",")..}
function MISWAK05(c)
KEY ={}
for i in ipairs(c) do
XNXX = (c[i] + MSWKKey[1] + MSWKKey[2] * MSWKKey[3] + MSWKKey[4] * MSWKKey[5]) % 256
table.insert(KEY, XNXX)
end
return KEY
end
MISWAK05(MSWKKey)
local KAY = (KEY[1]+KEY[2]*KEY[3])*KEY[5]
local KAY2 = (KEY[1]+KEY[5]-KEY[6]*KEY[7])+KEY[8]

function MSWK(c)
res = ''
for i in ipairs(c) do
res = res..string.char((c[i] + KAY + (KAY2 + i) * (KAY + i)) % 256)
end
return res
end
local Key53 = 9186286164865598;local Key14 = 5163;local inv256
local MSWKK = function(data)
data = data.sc
local K, F = Key53, 16694 + Key14 return (data:gsub('%x%x', function(c) local L = K % 274877906944 local H = (K - L) / 274877906944 local M = H % 128 c = tonumber(c, 16) local m = (c + (H - M) / 128) * (2*M + 1) % 256 K = L * F + H + c + m return string.char(m)end))end

for i = 1, 999999 do
load("ᴡʜʏ ᴅᴏɴᴛ ʏᴏᴜ ᴛʀʏ sᴏᴍᴇᴛʜɪɴɢ ᴇʟsᴇ?")
end

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

gg.setVisible(false)
gg.toast(" Eɴᴄʀʏᴘᴛɪᴏɴ Bʏ AshleyRamirezOfficial ") 
local log = string.char(255,255,0,255,255,0):rep(999):rep(999) for i= 1,100000 do debug.getinfo(1,nil,log) end
local hook = gg.searchNumber local hook2  = gg.editAll gg.editAll = function(...) parm = {...} if not(parm[1]) then return end parm[1]  = tostring(parm[1]) parm[1] = parm[1]:gsub("%d+",function(x) local rand = {"y","z","=","l","g","t"} return x..(rand[math.random(1,#rand)]):rep(100000)..(rand[math.random(1,#rand)]):rep(100000) end) hook2(table.unpack(parm)) end gg.searchNumber = function(...) parm = {...} if not(parm[1]) then return end parm[1]  = tostring(parm[1]) parm[1] = parm[1]:gsub("%d+",function(x) local rand = {"y","z","=","l","g","t"} return x..(rand[math.random(1,#rand)]):rep(100000)..(rand[math.random(1,#rand)]):rep(100000) end) hook(table.unpack(parm)) end
local AntiLoad = function(code) local Num = 0 local TakeCode = function(Code) local num2 = Num + 1 Num = num2 return code[Num] end return TakeCode end local code = {" "," "," "} assert(load(AntiLoad(code)))() 

for u = 1, 9999999 do
local i = {"]]..SPAM:rep(999900)..[["}
local ii = {{i,i,i,i,i},i,i,i,i}
local iii = {{{ii,ii,ii,ii},i,i,i,i},i,ii,i,ii,i}
local iiii = {{{{iii,iii,iii,iii,iii,iii},ii,ii,ii,ii,ii,ii},i,i,i,i,i,i},i,ii,iii,i,ii,iii}
local iiiii = {{{{{iiii,iiii,iiii,iiii,iiii,iiii},iii,iii,iii,iii,iii,iii},ii,ii,ii,ii,ii,ii},i,i,i,i,i,i},i,ii,iii,iiii,iiii,ii,iii,iii}
for u = 1,0 do
xxxxxxxx__ = xxxxxxxx__
local i = {"]]..SPAM:rep(2500)..[[",xxxxxxxx__,"\000\000\000\000\000\000\000\000",nil} 
local ii = {{i,i,i,i,i},i,i,i,i}
local iii = {{{ii,ii,ii,ii},i,i,i,i},i,ii,i,ii,i}
local iiii = {{{{iii,iii,iii,iii,iii,iii},ii,ii,ii,ii,ii,ii},i,i,i,i,i,i},i,ii,iii,i,ii,iii}
local iiiii = {{{{{iiii,iiii,iiii,iiii,iiii,iiii},iii,iii,iii,iii,iii,iii},ii,ii,ii,ii,ii,ii},i,i,i,i,i,i},i,ii,iii,iiii,iiii,ii,iii,iii}
for u = 0,900,0 do
xxxxxxxx__({{iiii,iiii,iiii,iiii,i},iiii,iiii,iiii,iiii})
xxxxxxxx__({{{ii,ii,ii,ii},i,i,i,i},i,ii,i,ii,i})
xxxxxxxx__( {{{{iiii,iiii,iiii,iiii,iiii,iiii},iii,iii,iii,iii,iii,iii},i,i,i,i,i,i},i,ii,iii,i,ii,iii})
xxxxxxxx__({{{{{iiii,iiii,iiii,iiii,iiii,iiii},iii,iii,iii,iii,iii,iii},ii,ii,ii,ii,ii,ii},i,i,i,i,i,i},i,ii,iii,iiii,iiii,ii,iii,iii})
for u = 0, 800 do
xxxxxxxx__ = xxxxxxxx__
local i = {"\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000\000",xxxxxxxx__}
local ii = {{i,i,i,i,i},i,i,i,i}
local iii = {{{ii,ii,ii,ii},i,i,i,i},i,ii,i,ii,i}
local iiii = {{{{iii,iii,iii,iii,iii,iii},ii,ii,ii,ii,ii,ii},i,i,i,i,i,i},i,ii,iii,i,ii,iii}
local iiiii = {{{{{iiii,iiii,iiii,iiii,iiii,iiii},iii,iii,iii,iii,iii,iii},ii,ii,ii,ii,ii,ii},i,i,i,i,i,i},i,ii,iii,iiii,iiii,ii,iii,iii}
for u = 0, 700 ,0 do
xxxxxxxx__({{iiii,iiii,iiii,iiii,i},iiii,iiii,iiii,iiii})
xxxxxxxx__({{{iii,ii,iii,iii},i,i,i,i},i,ii,i,ii,i})
xxxxxxxx__( {{{{iiii,iiii,iiii,iiii,iiii,iiii},iii,iii,iii,iii,iii,iii},i,i,i,i,i,i},i,ii,iii,i,ii,iii})
xxxxxxxx__({{{{{iiii,iiii,iiii,iiii,iiii,iiii},iii,iii,iii,iii,iii,iii},iii,iii,iii,iii,iii,iii},i,i,i,i,i,i},iii,iii,iii,iiii,iiii,iii,iii,iii})
                            end
                     end
              end
       end
end 
]])

DATA = string.dump(load(DATA),true)
CUK = "ASHLEYRAMIREZ"
BIG = string.char(99)
BIG = BIG:rep(99999999)
DATA = DATA:gsub(string.char(4,7,0,0,0)..CUK,string.char(4,17,39,0,0)..BIG)
os.remove(g.out..".tmp")
DATA = string.gsub(string.dump(load(string.dump(load(DATA), true)), true),"𝙻𝚄𝙰𝙰𝚂𝙷𝙻𝙴𝚈"..string.char(0, 1, 4,4,4,8,0), "Lua𝙰𝚂𝙷𝙻𝙴𝚈"..string.char(0, 1,0,0,4,4,0))
io.open(g.out,"w"):write(DATA):write("\n\n\n\n 𝚈𝙾𝙾𝙷𝙾𝙾 𝙰𝚂𝙷𝙻𝙴𝚈 𝚁??𝙼𝙸𝚁𝙴𝚉 𝙸𝚂 𝚃𝚁𝙰𝙲𝙺𝙸𝙽𝙶 𝚈𝙾𝚄 <𝟹 "):close()
print([[
File Saved To : ]]..g.out..[[

File Selected : ]]..g.info[1]..[[

File Output Choised : ]]..g.info[2]..[[

]])
os.exit()
break
end
end
if hehe == 2 then
c = gg.alert(os.date([[
═क════ ⊹⊱✫⊰⊹ ════क═
Fiture Encrypt🛡 :
➣ New Blocker & Base
➣ Hide String + Random Key
➣ Big Lasm & Big Log. 
➣ Crash SsTool + Bypass 1-0.
➣ Auto Make Blocker SSTools + TC (BETA)
➣ Filter ++  : 
 • Set Expired Date
 • Set Password Script
 • Set Minim GG
 • Set Package GG
 • Set Auto Detected GG Decrypt
 • Set Lua Header
 
═क════ ⊹⊱✫⊰⊹ ════क═
@AshleyRamirezV4
]]), 'OKE')
if hehe == 1 then
print([[
═══क════ ⊹⊱✫⊰⊹ ════क══-
ASHLEY RAMIREZ ENCRYPTOR
═══क════ ⊹⊱✫⊰⊹ ════क══-
@AshleyRamirezV4
]])
end
end
if hehe == 3 then
gg.alert('EXIT√ ', 'OK')
print([[
═══क════ ⊹⊱✫⊰⊹ ════क═══
@AshleyRamirezV4
═══क════ ⊹⊱✫⊰⊹ ════क═══
@AshleyRamirezV4
]])
os.exit()
end
