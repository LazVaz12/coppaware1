local ver = 'BETA'
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/youngchongosreal/coppaware/main/coppaware.lua"))()
local hub = Library:New("Coffeeware Premium " .. ver)
local Lighting = game:GetService("Lighting")
local UserInputService = game:GetService("UserInputService")
local InfoTab = hub:NewTab("Info")
local CreditsTab = hub:NewTab("Credits")
local ScriptsTab = hub:NewTab("Scripts")
hub:SetMainTab(InfoTab)

-- info here:

CreditsTab:NewLabel('This was originally just a bunch of slander')
CreditsTab:NewLabel('but honestly whatever imma remove it')
CreditsTab:NewLabel('I changed to Titanium Hub because fuck this idea')
CreditsTab:NewLabel('all the devs in coppaware were bad no offense')

-- credits here:

CreditsTab:NewLabel('Script developed and organized by me')
CreditsTab:NewLabel('UI stolen from Padero :troll:')
CreditsTab:NewLabel('Gun and jetpack script by Xenitrion. Not listing tag since')
CreditsTab:NewLabel('hes in a scandal where his dumbass put child porn as his pfp')
CreditsTab:NewLabel('and he says he didnt know abt it but whatever')
CreditsTab:NewLabel('Credit to Dave for volunteering but he hasnt done shit yet')

--[[ SCRIPTS HERE.

how to make buttons and labels and shit since your a skid lol:

local ScriptsTab = hub:NewTab("Scripts")
       v v v v
///// ScriptsTab:NewButton('name', 'description', function()
insert your code here
end)

]]--


-- anyways lolllllllllllll

-- gun script

ScriptsTab:NewButton('funny gun script', 'Made by Xenitrion. Hats are in #hats', function()
for i,v in next, game:GetService("Players").LocalPlayer.Character:GetDescendants() do
    if v:IsA("BasePart") and v.Name ~="HumanoidRootPart" then 
    game:GetService("RunService").Heartbeat:connect(function()
    v.Velocity = Vector3.new(-30,0,0)
    end)
    end
    end

    game:GetService("StarterGui"):SetCore("SendNotification", { 
        Title = "Notification";
        Text = "Netless Ran";
        Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150"})
    Duration = 16;

HumanDied = false
_G.ClickFling=false -- Set this to true if u want.
plr = game.Players.LocalPlayer
char=game.Players.LocalPlayer.Character
ct={}
te=table.insert

HumanDied=false

for i,v in next, game:GetService("Players").LocalPlayer.Character:GetDescendants() do
if v:IsA("BasePart") then 
te(ct,game:GetService("RunService").Heartbeat:connect(function()
pcall(function()
v.Velocity = Vector3.new(0,-30,0)
sethiddenproperty(game.Players.LocalPlayer,"MaximumSimulationRadius",math.huge)
sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",999999999)
game.Players.LocalPlayer.ReplicationFocus = workspace
end)
end))
end
end

function notify(t,tex,dur)
game.StarterGui:SetCore("SendNotification", {
    Title = t; 
    Text = tex; 
    Duration = dur or 5;
})
end

local srv= game:GetService("RunService")

fl=Instance.new('Folder',char);fl.Name='CWExtra'

char.Archivable = true
local reanim = char:Clone()
reanim.Name='NexoPD'

for i,v in next, reanim:GetDescendants() do
if v:IsA('BasePart') or v:IsA('Decal') then
v.Transparency = 1 
end 
end

--flinge = false

penis=5.65
plr.Character=nil
plr.Character=char
char.Humanoid.AutoRotate=false
char.Humanoid.WalkSpeed=0
char.Humanoid.JumpPower=0
char.Torso.Anchored = true
notify('Nexo','Reanimating...\nPlease wait '..penis..' seconds.')
wait(penis)
char.Torso.Anchored=false
notify('Nexo','Reanimated..')
char.Humanoid.Health=0
--reanim.Humanoid.AutoRotate=false
reanim.Animate.Disabled = true
reanim.Parent = fl
reanim.HumanoidRootPart.CFrame = char.HumanoidRootPart.CFrame*CFrame.new(0,5,0)

function create(part, parent, p, r)
Instance.new("Attachment",part)
Instance.new("AlignPosition",part)
Instance.new("AlignOrientation",part)
Instance.new("Attachment",parent)
part.Attachment.Name = part.Name
parent.Attachment.Name = part.Name
part.AlignPosition.Attachment0 = part[part.Name]
part.AlignOrientation.Attachment0 = part[part.Name]
part.AlignPosition.Attachment1 = parent[part.Name]
part.AlignOrientation.Attachment1 = parent[part.Name]
parent[part.Name].Position = p or Vector3.new()
part[part.Name].Orientation = r or Vector3.new()
part.AlignPosition.MaxForce = 999999999
part.AlignPosition.MaxVelocity = math.huge
part.AlignPosition.ReactionForceEnabled = false
part.AlignPosition.Responsiveness = math.huge
part.AlignOrientation.Responsiveness = math.huge
part.AlignPosition.RigidityEnabled = false
part.AlignOrientation.MaxTorque = 999999999
part.Massless=true
end

function Pos(part, parent, p)
Instance.new("Attachment",part)
Instance.new("AlignPosition",part)
Instance.new("Attachment",parent)
part.Attachment.Name = part.Name
parent.Attachment.Name = part.Name
part.AlignPosition.Attachment0 = part[part.Name]
--part.AlignOrientation.Attachment0 = part[part.Name]
part.AlignPosition.Attachment1 = parent[part.Name]
--part.AlignOrientation.Attachment1 = parent[part.Name]
parent[part.Name].Position = p or Vector3.new()
part.AlignPosition.MaxForce = 999999999
part.AlignPosition.MaxVelocity = math.huge
part.AlignPosition.ReactionForceEnabled = false
part.AlignPosition.Responsiveness = math.huge
--part.AlignOrientation.Responsiveness = math.huge
--part.AlignPosition.RigidityEnabled = false
--part.AlignOrientation.MaxTorque = 999999999
part.Massless=true
end

for i,part in next, char:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.RenderStepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, char:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.Stepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, reanim:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.RenderStepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, reanim:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.Stepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,v in next, char:GetDescendants() do
if v:IsA('Accessory') then
create(v.Handle,reanim[v.Name].Handle)
end
end

--Pos(fhrp,reanim['Torso'])
create(char['Head'],reanim['Head'])
create(char['Torso'],reanim['Torso'])
Pos(char['HumanoidRootPart'],reanim['Torso'],Vector3.new(0,0,0))
create(char['Right Arm'],reanim['Right Arm'])
create(char['Left Arm'],reanim['Left Arm'])
create(char['Right Leg'],reanim['Right Leg'])
create(char['Left Leg'],reanim['Left Leg'])

m = plr:GetMouse()

local LVecPart = Instance.new("Part", fl) LVecPart.CanCollide = false LVecPart.Transparency = 1

te(ct,srv.RenderStepped:Connect(function()
local lookVec = workspace.CurrentCamera.CFrame.lookVector
local Root = reanim["HumanoidRootPart"]
LVecPart.Position = Root.Position
LVecPart.CFrame = CFrame.new(LVecPart.Position, Vector3.new(lookVec.X * 10000, lookVec.Y, lookVec.Z * 10000))
end))

wdown=false
sdown=false
adown=false
ddown=false
spacedown=false

--reanim.HumanoidRootPart.RootJoint.Part0=nil

function flinger(p)
f=Instance.new('BodyAngularVelocity',p)
f.AngularVelocity = Vector3.new(9e9,9e9,9e9)
f.MaxTorque=Vector3.new(9e9,9e9,9e9)
end

flinger(char.HumanoidRootPart)

m=plr:GetMouse()

--char.HumanoidRootPart.Transparency = 0

bp=Instance.new('BodyPosition',char.HumanoidRootPart)
bp.P = 9e9
bp.D = 9e9
bp.MaxForce=Vector3.new(99999,99999,99999)

local click

te(ct,srv.Heartbeat:Connect(function()
if click == true then
bp.Position=m.Hit.p
char.HumanoidRootPart.Position=m.Hit.p
else
bp.Position=reanim.Torso.Position
char.HumanoidRootPart.Position=reanim.Torso.Position
end
end))

local Highlight = Instance.new("SelectionBox")
Highlight.Adornee = char.HumanoidRootPart
Highlight.LineThickness=0.05
Highlight.Color3 = Color3.fromRGB(30,255,30)
Highlight.Parent = char.HumanoidRootPart
Highlight.Name = "RAINBOW"

hrp = Highlight

spawn(function()
while true do
srv.Stepped:Wait()
if ded then break end
hrp.Color3 = Color3.new(255/255,0/255,0/255)
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(255/255,i/255,0/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(i/255,255/255,0/255)
end
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(0/255,255/255,i/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(0/255,i/255,255/255)
end
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(i/255,0/255,255/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(255/255,0/255,i/255)
end
end
end)

te(ct,m.Button1Down:Connect(function()
click=true
end))

te(ct,m.Button1Up:Connect(function()
click=false
end))

te(ct,m.KeyDown:Connect(function(e)
if e ==' ' then
spacedown=true end
if e =='w' then
wdown=true end
if e =='s' then
sdown=true end
if e =='a' then
adown=true end
if e =='d' then
ddown=true
end
end))

te(ct,m.KeyUp:Connect(function(e)
if e ==' ' then
spacedown=false end
if e =='w' then
wdown=false end
if e =='s' then
sdown=false end
if e =='a' then
adown=false end
if e =='d' then
ddown=false
end
end))

local function MoveClone(X,Y,Z)
LVecPart.CFrame = LVecPart.CFrame * CFrame.new(-X,Y,-Z)
reanim.Humanoid.WalkToPoint = LVecPart.Position
end

te(ct,srv.RenderStepped:Connect(function()
if wdown==true then
MoveClone(0,0,1e4) end
if sdown==true then
MoveClone(0,0,-1e4) end
if adown==true then
MoveClone(1e4,0,0) end
if ddown==true then
MoveClone(-1e4,0,0)
end
if spacedown==true then
reanim.Humanoid.Jump=true end
if wdown ~= true and adown ~= true and sdown ~= true and ddown ~= true then
reanim.Humanoid.WalkToPoint = reanim.HumanoidRootPart.Position end
end))

--reanim.HumanoidRootPart.RootJoint.Part1=nil

workspace.CurrentCamera.CameraSubject = reanim.Humanoid

reset=Instance.new('BindableEvent')
te(ct,reset.Event:Connect(function()
reanim:Destroy()
HumanDied=true
reanimated=false
for i,v in next, char:GetDescendants() do if v:IsA('BasePart') then v.Anchored=true end end
hc=char.Humanoid:Clone()
char.Humanoid:Destroy()
hc.Parent=char
game.Players:Chat('-re')
for i,v in pairs(ct) do v:Disconnect() end
game:GetService("StarterGui"):SetCore("ResetButtonCallback", true)
reset:Remove()
end))

game:GetService("StarterGui"):SetCore("ResetButtonCallback", reset)

IT = Instance.new
CF = CFrame.new
VT = Vector3.new
RAD = math.rad
C3 = Color3.new
UD2 = UDim2.new
BRICKC = BrickColor.new
ANGLES = CFrame.Angles
EULER = CFrame.fromEulerAnglesXYZ
COS = math.cos
ACOS = math.acos
SIN = math.sin
ASIN = math.asin
ABS = math.abs
MRANDOM = math.random
FLOOR = math.floor

speed = 1
sine = 1
srv = game:GetService('RunService')

function hatset(yes,part,c1,c0,nm)
reanim[yes].Handle.AccessoryWeld.Part1=reanim[part]
reanim[yes].Handle.AccessoryWeld.C1=c1 or CFrame.new()
reanim[yes].Handle.AccessoryWeld.C0=c0 or CFrame.new()--3bbb322dad5929d0d4f25adcebf30aa5
if nm==true then
for i,v in next, workspace[game.Players.LocalPlayer.Name][yes].Handle:GetDescendants() do
if v:IsA('Mesh') or v:IsA('SpecialMesh') then
v:Remove()
end
end
end
end

function setuptrail(parent,Pos1,Pos2,Color,LT,LE,Texture)
IT = Instance.new
local Part1 = parent
local A1 = IT("Attachment",Part1)
A1.Position = Pos1
A1.Name = "ATH10"
local B1 = IT("Attachment",Part1)
B1.Position = Pos2
B1.Name = "ATH11"
local Trail1 = IT("Trail",Part1)
Trail1.Name = "Nexo Trail"
Trail1.Color = Color
Trail1.Attachment0 = B1
Trail1.Attachment1 = A1
Trail1.Lifetime = LT
Trail1.LightEmission = LE
Trail1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0, 0),NumberSequenceKeypoint.new(1, 1)})
Trail1.Texture = Texture
Trail1.Enabled = true
end

--                          |
--put the setup trail below v

--put the hat script converted below

reanim = game.Players.LocalPlayer.Character.CWExtra.NexoPD
RJ = reanim.HumanoidRootPart.RootJoint
RS = reanim.Torso['Right Shoulder']
LS = reanim.Torso['Left Shoulder']
RH = reanim.Torso['Right Hip']
LH = reanim.Torso['Left Hip']
Root = reanim.HumanoidRootPart
NECK = reanim.Torso.Neck
NECK.C0 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
NECK.C1 = CF(0,-0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C1 = CF(0,-1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C1 = CF(0,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C1 = CF(0,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))

Mode='1'

mousechanger=game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(k)
if k == 'q' then-- first mode
Mode='1'
elseif k == 'z' then-- second mode
Mode='2'
elseif k == 'x' then-- third mode
Mode='3'
elseif k == 'c' then-- fourth mode
Mode='4'
elseif k == 'v' then-- fourth mode
Mode='5'
elseif k == 'f' then-- fourth mode
Mode='6'
end
end)

coroutine.wrap(function()
while true do -- anim changer
if HumanDied then mousechanger:Disconnect() break end
sine = sine + speed
local rlegray = Ray.new(reanim["Right Leg"].Position + Vector3.new(0, 0.5, 0), Vector3.new(0, -2, 0))
local rlegpart, rlegendPoint = workspace:FindPartOnRay(rlegray, char)
local llegray = Ray.new(reanim["Left Leg"].Position + Vector3.new(0, 0.5, 0), Vector3.new(0, -2, 0))
local llegpart, llegendPoint = workspace:FindPartOnRay(llegray, char)
local rightvector = (Root.Velocity * Root.CFrame.rightVector).X + (Root.Velocity * Root.CFrame.rightVector).Z
local lookvector = (Root.Velocity * Root.CFrame.lookVector).X + (Root.Velocity * Root.CFrame.lookVector).Z
if lookvector > reanim.Humanoid.WalkSpeed then
lookvector = reanim.Humanoid.WalkSpeed
end
if lookvector < -reanim.Humanoid.WalkSpeed then
lookvector = -reanim.Humanoid.WalkSpeed
end
if rightvector > reanim.Humanoid.WalkSpeed then
rightvector = reanim.Humanoid.WalkSpeed
end
if rightvector < -reanim.Humanoid.WalkSpeed then
rightvector = -reanim.Humanoid.WalkSpeed
end
local lookvel = lookvector / reanim.Humanoid.WalkSpeed
local rightvel = rightvector / reanim.Humanoid.WalkSpeed
if Mode == '1' then
if Root.Velocity.y > 1 then -- jump
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1,-3.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.cos(sine/13)),RAD(90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.sin(sine/13)),RAD(90+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-40+3*math.sin(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(85+3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(-10+5*math.cos(sine/25)),math.rad(100+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(10+-5*math.cos(sine/25)),math.rad(-100+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(40+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(-40+0*math.cos(sine/10))),.2)
elseif Root.Velocity.y < -1 then -- fall
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1,-3.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.cos(sine/13)),RAD(90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.sin(sine/13)),RAD(90+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-40+3*math.sin(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(85+3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(-10+5*math.cos(sine/25)),math.rad(100+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(10+-5*math.cos(sine/25)),math.rad(-100+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(40+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(-40+0*math.cos(sine/10))),.2)
elseif Root.Velocity.Magnitude < 2 then -- idle
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1,-3.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.cos(sine/13)),RAD(90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.sin(sine/13)),RAD(90+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-40+3*math.sin(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(85+3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(-10+5*math.cos(sine/25)),math.rad(100+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(10+-5*math.cos(sine/25)),math.rad(-100+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(40+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(-40+0*math.cos(sine/10))),.2)
elseif Root.Velocity.Magnitude < 51 then -- walk
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1,-3.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.cos(sine/13)),RAD(90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.3*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/13)),RAD(70+-5*math.sin(sine/13)),RAD(90+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-40+3*math.sin(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(85+3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(-10+5*math.cos(sine/25)),math.rad(100+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+0*math.cos(sine/10)),math.rad(10+-5*math.cos(sine/25)),math.rad(-100+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(40+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-3*math.cos(sine/25)),math.rad(0+0*math.cos(sine/10)),math.rad(-40+0*math.cos(sine/10))),.2)
elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
elseif Mode == '2' then
if Root.Velocity.y > 1 then -- jump
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1.75,-2.3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.sin(sine/5),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(110+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(-10+10*math.cos(sine/5)),math.rad(100+0*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(10+-10*math.cos(sine/5)),math.rad(-100+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(40+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-40+0*math.cos(sine/5))),.2)
elseif Root.Velocity.y < -1 then -- fall
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1.75,-2.3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.sin(sine/5),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(110+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(-10+10*math.cos(sine/5)),math.rad(100+0*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(10+-10*math.cos(sine/5)),math.rad(-100+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(40+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-40+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 2 then -- idle
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1.75,-2.3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.sin(sine/5),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(110+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(-10+10*math.cos(sine/5)),math.rad(100+0*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(10+-10*math.cos(sine/5)),math.rad(-100+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(40+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-40+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 51 then -- walk
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-1.75,-2.3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1*math.cos(sine/5),0+0.15*math.sin(sine/5),0+0*math.sin(sine/13))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(75+-10*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(110+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(-10+10*math.cos(sine/5)),math.rad(100+0*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0.5+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-30+5*math.cos(sine/5)),math.rad(10+-10*math.cos(sine/5)),math.rad(-100+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(40+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(-40+30*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-40+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
elseif Mode == '3' then
if Root.Velocity.y > 1 then -- jump
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,0.3,-2.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(100+-15*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-1.1+0*math.cos(sine/5),0+-0.5*math.cos(sine/5))*CFrame.Angles(math.rad(140+0*math.cos(sine/5)),math.rad(-180+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(30+-10*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-30+10*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(-5+0*math.cos(sine/5)),math.rad(10+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(5+0*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2)
elseif Root.Velocity.y < -1 then -- fall
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,0.3,-2.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(100+-15*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-1.1+0*math.cos(sine/5),0+-0.5*math.cos(sine/5))*CFrame.Angles(math.rad(140+0*math.cos(sine/5)),math.rad(-180+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(30+-10*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-30+10*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(-5+0*math.cos(sine/5)),math.rad(10+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(5+0*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 2 then -- idle
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,0.3,-2.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(100+-15*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-1.1+0*math.cos(sine/5),0+-0.5*math.cos(sine/5))*CFrame.Angles(math.rad(140+0*math.cos(sine/5)),math.rad(-180+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(30+-10*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-30+10*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(-5+0*math.cos(sine/5)),math.rad(10+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(5+0*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 51 then -- walk
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,0.3,-2.5),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.cos(sine/5)),RAD(90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+1*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(60+20*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(100+-15*math.sin(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.sin(sine/5))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-1.1+0*math.cos(sine/5),0+-0.5*math.cos(sine/5))*CFrame.Angles(math.rad(140+0*math.cos(sine/5)),math.rad(-180+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(30+-10*math.cos(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),1.3+0*math.cos(sine/5),0.3+0*math.cos(sine/5))*CFrame.Angles(math.rad(230+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(-30+10*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(-5+0*math.cos(sine/5)),math.rad(10+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0*math.cos(sine/5),0+0*math.cos(sine/5))*CFrame.Angles(math.rad(130+15*math.cos(sine/5)),math.rad(5+0*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
elseif Mode == '4' then
if Root.Velocity.y > 1 then -- jump
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,1,-0.2),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.cos(sine/5)),RAD(-90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(30+-25*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),3+-1.5*math.cos(sine/5),0+-0.3*math.cos(sine/5))*CFrame.Angles(math.rad(30+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-10+30*math.cos(sine/5)),math.rad(10+0*math.sin(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(10+-30*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-20+-30*math.cos(sine/5)),math.rad(20+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(20+30*math.cos(sine/5)),math.rad(-20+0*math.cos(sine/5))),.2)
elseif Root.Velocity.y < -1 then -- fall
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,1,-0.2),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.cos(sine/5)),RAD(-90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(30+-25*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),3+-1.5*math.cos(sine/5),0+-0.3*math.cos(sine/5))*CFrame.Angles(math.rad(30+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-10+30*math.cos(sine/5)),math.rad(10+0*math.sin(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(10+-30*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-20+-30*math.cos(sine/5)),math.rad(20+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(20+30*math.cos(sine/5)),math.rad(-20+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 2 then -- idle
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,1,-0.2),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.cos(sine/5)),RAD(-90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(30+-25*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),3+-1.5*math.cos(sine/5),0+-0.3*math.cos(sine/5))*CFrame.Angles(math.rad(30+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-10+30*math.cos(sine/5)),math.rad(10+0*math.sin(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(10+-30*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-20+-30*math.cos(sine/5)),math.rad(20+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(20+30*math.cos(sine/5)),math.rad(-20+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 51 then -- walk
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,1,-0.2),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.cos(sine/5)),RAD(-90+0*math.cos(sine/5))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+2*math.cos(sine/5),0+-0.5*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(-90+0*math.cos(sine/5)),RAD(0+-20*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(30+-25*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),3+-1.5*math.cos(sine/5),0+-0.3*math.cos(sine/5))*CFrame.Angles(math.rad(30+-10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-10+30*math.cos(sine/5)),math.rad(10+0*math.sin(sine/5))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(10+-30*math.cos(sine/5)),math.rad(-10+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(-20+-30*math.cos(sine/5)),math.rad(20+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+25*math.sin(sine/5)),math.rad(20+30*math.cos(sine/5)),math.rad(-20+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
elseif Mode == '5' then
if Root.Velocity.y > 1 then -- jump
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+-1*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(-105+0*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(80+-20*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+0*math.cos(sine/5),0+0.5*math.cos(sine/5))*CFrame.Angles(math.rad(-80+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.y < -1 then -- fall
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+-1*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(-105+0*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(80+-20*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+0*math.cos(sine/5),0+0.5*math.cos(sine/5))*CFrame.Angles(math.rad(-80+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 2 then -- idle
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,-2.1,0.3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+-1*math.cos(sine/5),0+0*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(-105+0*math.cos(sine/5)),RAD(90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+-1*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(-105+0*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(80+-20*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+0*math.cos(sine/5),0+0.5*math.cos(sine/5))*CFrame.Angles(math.rad(-80+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 20 then -- walk
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+-1*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(-105+0*math.sin(sine/5)),RAD(90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(80+-20*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/5),-2+0*math.cos(sine/5),0+0.5*math.cos(sine/5))*CFrame.Angles(math.rad(-80+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),1+0*math.cos(sine/10),-0.5+0*math.cos(sine/10))*CFrame.Angles(math.rad(140+10*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-0.5+0.5*math.cos(sine/5),-0.7+-0.1*math.cos(sine/5))*CFrame.Angles(math.rad(-10+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
elseif Mode == '6' then
if Root.Velocity.y > 1 then -- jump
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,2.5,-3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.cos(sine/5)),RAD(-90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(60+-10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+-15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.y < -1 then -- fall
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,2.5,-3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.cos(sine/5)),RAD(-90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(60+-10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+-15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 2 then -- idle
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,2.5,-3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.cos(sine/5)),RAD(-90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(60+-10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+-15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude < 20 then -- walk
hatset('Meshes/HeavySniper (1)Accessory','HumanoidRootPart',CFrame.new(0,2.5,-3),reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.cos(sine/5),0+0*math.cos(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.cos(sine/5)),RAD(-90+0*math.cos(sine/13))),1),false)
reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0 = reanim['Meshes/HeavySniper (1)Accessory'].Handle.AccessoryWeld.C0:Lerp(CF(0+1.5*math.cos(sine/5),0+0*math.sin(sine/5),0+0*math.sin(sine/5))*ANGLES(RAD(90+0*math.cos(sine/5)),RAD(145+10*math.sin(sine/5)),RAD(-90+0*math.sin(sine/5))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(60+-10*math.sin(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.sin(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),-2+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+-15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/5),0+0.245*math.cos(sine/5),-1+0.245*math.cos(sine/5))*CFrame.Angles(math.rad(50+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/5),-1+0.3*math.cos(sine/5),-1+0*math.cos(sine/5))*CFrame.Angles(math.rad(-60+15*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5)),math.rad(0+0*math.cos(sine/5))),.2)
elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
end
srv.RenderStepped:Wait()
end
end)()
end)

-- JETPACK script!!!

-- xd xd xd thrust

ScriptsTab:NewButton('fe thruster', 'jetpack!', function()
for i,v in next, game:GetService("Players").LocalPlayer.Character:GetDescendants() do
    if v:IsA("BasePart") and v.Name ~="HumanoidRootPart" then 
    game:GetService("RunService").Heartbeat:connect(function()
    v.Velocity = Vector3.new(-30,0,0)
    end)
    end
    end

    game:GetService("StarterGui"):SetCore("SendNotification", { 
        Title = "Notification";
        Text = "Netless Ran";
        Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150"})
    Duration = 16;

game:GetService("Players").LocalPlayer.Character["Hat1"].Handle:FindFirstChildOfClass("SpecialMesh"):Destroy()
game:GetService("Players").LocalPlayer.Character["Pal Hair"].Handle:FindFirstChildOfClass("SpecialMesh"):Destroy()
game:GetService("Players").LocalPlayer.Character["RobloxVisor2019"].Handle:FindFirstChildOfClass("SpecialMesh"):Destroy()
game:GetService("Players").LocalPlayer.Character["SamuraiHat"].Handle:FindFirstChildOfClass("SpecialMesh"):Destroy()
LocalPlayer = game:GetService("Players").LocalPlayer
LocalPlayer.Character.Humanoid.WalkSpeed = 70
LocalPlayer.Character.Humanoid.JumpPower = 85

HumanDied = false
_G.ClickFling = false -- Set this to true if u want.
plr = game.Players.LocalPlayer
char=game.Players.LocalPlayer.Character
ct={}
te=table.insert

HumanDied=false

for i,v in next, game:GetService("Players").LocalPlayer.Character:GetDescendants() do
if v:IsA("BasePart") then 
te(ct,game:GetService("RunService").Heartbeat:connect(function()
pcall(function()
v.Velocity = Vector3.new(0,-30,0)
sethiddenproperty(game.Players.LocalPlayer,"MaximumSimulationRadius",math.huge)
sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",999999999)
game.Players.LocalPlayer.ReplicationFocus = workspace
end)
end))
end
end

function notify(t,tex,dur)
game.StarterGui:SetCore("SendNotification", {
    Title = t; 
    Text = tex; 
    Duration = dur or 5;
})
end

local srv= game:GetService("RunService")

fl=Instance.new('Folder',char);fl.Name='CWExtra'

char.Archivable = true
local reanim = char:Clone()
reanim.Name='NexoPD'

for i,v in next, reanim:GetDescendants() do
if v:IsA('BasePart') or v:IsA('Decal') then
v.Transparency = 1 
end 
end

--flinge = false

penis=5.65
plr.Character=nil
plr.Character=char
char.Humanoid.AutoRotate=false
char.Humanoid.WalkSpeed=0
char.Humanoid.JumpPower=0
char.Torso.Anchored = true
notify('Nexo','Reanimating...\nPlease wait '..penis..' seconds.')
wait(penis)
char.Torso.Anchored=false
notify('Nexo','Reanimated..')
char.Humanoid.Health=0
--reanim.Humanoid.AutoRotate=false
reanim.Animate.Disabled = true
reanim.Parent = fl
reanim.HumanoidRootPart.CFrame = char.HumanoidRootPart.CFrame*CFrame.new(0,5,0)

function create(part, parent, p, r)
Instance.new("Attachment",part)
Instance.new("AlignPosition",part)
Instance.new("AlignOrientation",part)
Instance.new("Attachment",parent)
part.Attachment.Name = part.Name
parent.Attachment.Name = part.Name
part.AlignPosition.Attachment0 = part[part.Name]
part.AlignOrientation.Attachment0 = part[part.Name]
part.AlignPosition.Attachment1 = parent[part.Name]
part.AlignOrientation.Attachment1 = parent[part.Name]
parent[part.Name].Position = p or Vector3.new()
part[part.Name].Orientation = r or Vector3.new()
part.AlignPosition.MaxForce = 999999999
part.AlignPosition.MaxVelocity = math.huge
part.AlignPosition.ReactionForceEnabled = false
part.AlignPosition.Responsiveness = math.huge
part.AlignOrientation.Responsiveness = math.huge
part.AlignPosition.RigidityEnabled = false
part.AlignOrientation.MaxTorque = 999999999
part.Massless=true
end

function Pos(part, parent, p)
Instance.new("Attachment",part)
Instance.new("AlignPosition",part)
Instance.new("Attachment",parent)
part.Attachment.Name = part.Name
parent.Attachment.Name = part.Name
part.AlignPosition.Attachment0 = part[part.Name]
--part.AlignOrientation.Attachment0 = part[part.Name]
part.AlignPosition.Attachment1 = parent[part.Name]
--part.AlignOrientation.Attachment1 = parent[part.Name]
parent[part.Name].Position = p or Vector3.new()
part.AlignPosition.MaxForce = 999999999
part.AlignPosition.MaxVelocity = math.huge
part.AlignPosition.ReactionForceEnabled = false
part.AlignPosition.Responsiveness = math.huge
--part.AlignOrientation.Responsiveness = math.huge
--part.AlignPosition.RigidityEnabled = false
--part.AlignOrientation.MaxTorque = 999999999
part.Massless=true
end

for i,part in next, char:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.RenderStepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, char:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.Stepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, reanim:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.RenderStepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, reanim:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.Stepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,v in next, char:GetDescendants() do
if v:IsA('Accessory') then
create(v.Handle,reanim[v.Name].Handle)
end
end

--Pos(fhrp,reanim['Torso'])
create(char['Head'],reanim['Head'])
create(char['Torso'],reanim['Torso'])
Pos(char['HumanoidRootPart'],reanim['Torso'],Vector3.new(0,0,0))
create(char['Right Arm'],reanim['Right Arm'])
create(char['Left Arm'],reanim['Left Arm'])
create(char['Right Leg'],reanim['Right Leg'])
create(char['Left Leg'],reanim['Left Leg'])

m = plr:GetMouse()

local LVecPart = Instance.new("Part", fl) LVecPart.CanCollide = false LVecPart.Transparency = 1

te(ct,srv.RenderStepped:Connect(function()
local lookVec = workspace.CurrentCamera.CFrame.lookVector
local Root = reanim["HumanoidRootPart"]
LVecPart.Position = Root.Position
LVecPart.CFrame = CFrame.new(LVecPart.Position, Vector3.new(lookVec.X * 10000, lookVec.Y, lookVec.Z * 10000))
end))

wdown=false
sdown=false
adown=false
ddown=false
spacedown=false

--reanim.HumanoidRootPart.RootJoint.Part0=nil

function flinger(p)
f=Instance.new('BodyAngularVelocity',p)
f.AngularVelocity = Vector3.new(9e9,9e9,9e9)
f.MaxTorque=Vector3.new(9e9,9e9,9e9)
end

flinger(char.HumanoidRootPart)

m=plr:GetMouse()

--char.HumanoidRootPart.Transparency = 0

bp=Instance.new('BodyPosition',char.HumanoidRootPart)
bp.P = 9e9
bp.D = 9e9
bp.MaxForce=Vector3.new(99999,99999,99999)

local click

te(ct,srv.Heartbeat:Connect(function()
if click == true then
bp.Position=m.Hit.p
char.HumanoidRootPart.Position=m.Hit.p
else
bp.Position=reanim.Torso.Position
char.HumanoidRootPart.Position=reanim.Torso.Position
end
end))

local Highlight = Instance.new("SelectionBox")
Highlight.Adornee = char.HumanoidRootPart
Highlight.LineThickness=0.05
Highlight.Color3 = Color3.fromRGB(30,255,30)
Highlight.Parent = char.HumanoidRootPart
Highlight.Name = "RAINBOW"

hrp = Highlight

spawn(function()
while true do
srv.Stepped:Wait()
if ded then break end
hrp.Color3 = Color3.new(255/255,0/255,0/255)
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(255/255,i/255,0/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(i/255,255/255,0/255)
end
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(0/255,255/255,i/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(0/255,i/255,255/255)
end
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(i/255,0/255,255/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(255/255,0/255,i/255)
end
end
end)

te(ct,m.Button1Down:Connect(function()
click=true
end))

te(ct,m.Button1Up:Connect(function()
click=false
end))

te(ct,m.KeyDown:Connect(function(e)
if e ==' ' then
spacedown=true end
if e =='w' then
wdown=true end
if e =='s' then
sdown=true end
if e =='a' then
adown=true end
if e =='d' then
ddown=true
end
end))

te(ct,m.KeyUp:Connect(function(e)
if e ==' ' then
spacedown=false end
if e =='w' then
wdown=false end
if e =='s' then
sdown=false end
if e =='a' then
adown=false end
if e =='d' then
ddown=false
end
end))

local function MoveClone(X,Y,Z)
LVecPart.CFrame = LVecPart.CFrame * CFrame.new(-X,Y,-Z)
reanim.Humanoid.WalkToPoint = LVecPart.Position
end

te(ct,srv.RenderStepped:Connect(function()
if wdown==true then
MoveClone(0,0,1e4) end
if sdown==true then
MoveClone(0,0,-1e4) end
if adown==true then
MoveClone(1e4,0,0) end
if ddown==true then
MoveClone(-1e4,0,0)
end
if spacedown==true then
reanim.Humanoid.Jump=true end
if wdown ~= true and adown ~= true and sdown ~= true and ddown ~= true then
reanim.Humanoid.WalkToPoint = reanim.HumanoidRootPart.Position end
end))

--reanim.HumanoidRootPart.RootJoint.Part1=nil

workspace.CurrentCamera.CameraSubject = reanim.Humanoid

reset=Instance.new('BindableEvent')
te(ct,reset.Event:Connect(function()
reanim:Destroy()
HumanDied=true
reanimated=false
for i,v in next, char:GetDescendants() do if v:IsA('BasePart') then v.Anchored=true end end
hc=char.Humanoid:Clone()
char.Humanoid:Destroy()
hc.Parent=char
game.Players:Chat('-re')
for i,v in pairs(ct) do v:Disconnect() end
game:GetService("StarterGui"):SetCore("ResetButtonCallback", true)
reset:Remove()
end))

game:GetService("StarterGui"):SetCore("ResetButtonCallback", reset)

IT = Instance.new
CF = CFrame.new
VT = Vector3.new
RAD = math.rad
C3 = Color3.new
UD2 = UDim2.new
BRICKC = BrickColor.new
ANGLES = CFrame.Angles
EULER = CFrame.fromEulerAnglesXYZ
COS = math.cos
ACOS = math.acos
SIN = math.sin
ASIN = math.asin
ABS = math.abs
MRANDOM = math.random
FLOOR = math.floor

speed = 1
sine = 1
srv = game:GetService('RunService')

function hatset(yes,part,c1,c0,nm)
reanim[yes].Handle.AccessoryWeld.Part1=reanim[part]
reanim[yes].Handle.AccessoryWeld.C1=c1 or CFrame.new()
reanim[yes].Handle.AccessoryWeld.C0=c0 or CFrame.new()--3bbb322dad5929d0d4f25adcebf30aa5
if nm==true then
for i,v in next, workspace[game.Players.LocalPlayer.Name][yes].Handle:GetDescendants() do
if v:IsA('Mesh') or v:IsA('SpecialMesh') then
v:Remove()
end
end
end
end

function setuptrail(parent,Pos1,Pos2,Color,LT,LE,Texture)
IT = Instance.new
local Part1 = parent
local A1 = IT("Attachment",Part1)
A1.Position = Pos1
A1.Name = "ATH10"
local B1 = IT("Attachment",Part1)
B1.Position = Pos2
B1.Name = "ATH11"
local Trail1 = IT("Trail",Part1)
Trail1.Name = "Nexo Trail"
Trail1.Color = Color
Trail1.Attachment0 = B1
Trail1.Attachment1 = A1
Trail1.Lifetime = LT
Trail1.LightEmission = LE
Trail1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0, 0),NumberSequenceKeypoint.new(1, 1)})
Trail1.Texture = Texture
Trail1.Enabled = true
end

--                          |
--put the setup trail below v

--put the hat script converted below

reanim = game.Players.LocalPlayer.Character.CWExtra.NexoPD
RJ = reanim.HumanoidRootPart.RootJoint
RS = reanim.Torso['Right Shoulder']
LS = reanim.Torso['Left Shoulder']
RH = reanim.Torso['Right Hip']
LH = reanim.Torso['Left Hip']
Root = reanim.HumanoidRootPart
NECK = reanim.Torso.Neck
NECK.C0 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
NECK.C1 = CF(0,-0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C1 = CF(0,-1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C1 = CF(0,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C1 = CF(0,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))

Mode='1'

mousechanger=game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(k)
if k == 'z' then-- first mode
Mode='1'
end
end)

coroutine.wrap(function()
while true do -- anim changer
if HumanDied then mousechanger:Disconnect() break end
sine = sine + speed
local rlegray = Ray.new(reanim["Right Leg"].Position + Vector3.new(0, 0.5, 0), Vector3.new(0, -2, 0))
local rlegpart, rlegendPoint = workspace:FindPartOnRay(rlegray, char)
local llegray = Ray.new(reanim["Left Leg"].Position + Vector3.new(0, 0.5, 0), Vector3.new(0, -2, 0))
local llegpart, llegendPoint = workspace:FindPartOnRay(llegray, char)
local rightvector = (Root.Velocity * Root.CFrame.rightVector).X + (Root.Velocity * Root.CFrame.rightVector).Z
local lookvector = (Root.Velocity * Root.CFrame.lookVector).X + (Root.Velocity * Root.CFrame.lookVector).Z
if lookvector > reanim.Humanoid.WalkSpeed then
lookvector = reanim.Humanoid.WalkSpeed
end
if lookvector < -reanim.Humanoid.WalkSpeed then
lookvector = -reanim.Humanoid.WalkSpeed
end
if rightvector > reanim.Humanoid.WalkSpeed then
rightvector = reanim.Humanoid.WalkSpeed
end
if rightvector < -reanim.Humanoid.WalkSpeed then
rightvector = -reanim.Humanoid.WalkSpeed
end
local lookvel = lookvector / reanim.Humanoid.WalkSpeed
local rightvel = rightvector / reanim.Humanoid.WalkSpeed
if Mode == '1' then
if Root.Velocity.y > 1.5 then -- jump
hatset('Hat1','Torso',CFrame.new(),reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Hat1'].Handle.AccessoryWeld.C0 = reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('Pal Hair','Torso',CFrame.new(),reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Pal Hair'].Handle.AccessoryWeld.C0 = reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('RobloxVisor2019','Torso',CFrame.new(),reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0 = reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('SamuraiHat','Torso',CFrame.new(),reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.cos(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(180+0*math.cos(sine/13))),1),false)
reanim['SamuraiHat'].Handle.AccessoryWeld.C0 = reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.sin(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(180+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(60+-10*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.sin(sine/50),3+0.75*math.cos(sine/20),0+0*math.cos(sine/2))*CFrame.Angles(math.rad(-40+10*math.sin(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(20+-5*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(20+-5*math.cos(sine/20))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(20+-5*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(-20+5*math.cos(sine/20))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+-5*math.cos(sine/20)),math.rad(-10+0*math.cos(sine/10)),math.rad(5+0*math.cos(sine/20))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-40+-5*math.cos(sine/20)),math.rad(10+0*math.cos(sine/10)),math.rad(-5+0*math.cos(sine/10))),.2)
elseif Root.Velocity.y < -1.5 then -- fall
hatset('Hat1','Torso',CFrame.new(),reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Hat1'].Handle.AccessoryWeld.C0 = reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('Pal Hair','Torso',CFrame.new(),reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Pal Hair'].Handle.AccessoryWeld.C0 = reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('RobloxVisor2019','Torso',CFrame.new(),reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0 = reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('SamuraiHat','Torso',CFrame.new(),reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.cos(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(180+0*math.cos(sine/13))),1),false)
reanim['SamuraiHat'].Handle.AccessoryWeld.C0 = reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.sin(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(180+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(60+-10*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.sin(sine/50),3+0.75*math.cos(sine/20),0+0*math.cos(sine/2))*CFrame.Angles(math.rad(-110+10*math.sin(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+-5*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(20+-5*math.cos(sine/20))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-30+-5*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(-20+5*math.cos(sine/20))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-15+-5*math.cos(sine/20)),math.rad(-10+0*math.cos(sine/10)),math.rad(5+0*math.cos(sine/20))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-20+-5*math.cos(sine/20)),math.rad(10+0*math.cos(sine/10)),math.rad(-5+0*math.cos(sine/10))),.2)
elseif Root.Velocity.Magnitude < 2 then -- idle
hatset('Hat1','Torso',CFrame.new(),reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Hat1'].Handle.AccessoryWeld.C0 = reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('Pal Hair','Torso',CFrame.new(),reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Pal Hair'].Handle.AccessoryWeld.C0 = reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('RobloxVisor2019','Torso',CFrame.new(),reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0 = reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('SamuraiHat','Torso',CFrame.new(),reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.cos(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(180+0*math.cos(sine/13))),1),false)
reanim['SamuraiHat'].Handle.AccessoryWeld.C0 = reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.sin(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(180+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+-10*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),3+1*math.cos(sine/20),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(0+10*math.sin(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(10+-15*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(20+-15*math.cos(sine/20))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(10+-15*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(-20+15*math.cos(sine/20))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-15+-10*math.cos(sine/20)),math.rad(-10+0*math.cos(sine/10)),math.rad(5+0*math.cos(sine/20))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-20+-10*math.cos(sine/20)),math.rad(10+0*math.cos(sine/10)),math.rad(-5+0*math.cos(sine/10))),.2)
elseif Root.Velocity.Magnitude < 75 then -- walk
hatset('Hat1','Torso',CFrame.new(),reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Hat1'].Handle.AccessoryWeld.C0 = reanim['Hat1'].Handle.AccessoryWeld.C0:Lerp(CF(-0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('Pal Hair','Torso',CFrame.new(),reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['Pal Hair'].Handle.AccessoryWeld.C0 = reanim['Pal Hair'].Handle.AccessoryWeld.C0:Lerp(CF(0.8+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('RobloxVisor2019','Torso',CFrame.new(),reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),false)
reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0 = reanim['RobloxVisor2019'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.7+0*math.sin(sine/13),0+0*math.sin(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(0+0*math.sin(sine/13))),.3)
hatset('SamuraiHat','Torso',CFrame.new(),reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.cos(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(180+0*math.cos(sine/13))),1),false)
reanim['SamuraiHat'].Handle.AccessoryWeld.C0 = reanim['SamuraiHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),0.25+0*math.sin(sine/13),-0.5+0*math.sin(sine/13))*ANGLES(RAD(35+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13)),RAD(180+0*math.sin(sine/13))),.3)
NECK.C0=NECK.C0:Lerp(CFrame.new(0+0*math.cos(sine/10),1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(60+-10*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RJ.C0=RJ.C0:Lerp(CFrame.new(0+0*math.sin(sine/50),3+0.75*math.cos(sine/20),0+0*math.cos(sine/2))*CFrame.Angles(math.rad(-75+10*math.sin(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(0+0*math.cos(sine/10))),.2) 
RS.C0=RS.C0:Lerp(CFrame.new(1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-20+-5*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(20+-5*math.cos(sine/20))),.2) 
LS.C0=LS.C0:Lerp(CFrame.new(-1.5+0*math.cos(sine/10),0.5+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-20+-5*math.cos(sine/20)),math.rad(0+0*math.cos(sine/10)),math.rad(-20+5*math.cos(sine/20))),.2) 
RH.C0=RH.C0:Lerp(CFrame.new(0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-15+-5*math.cos(sine/20)),math.rad(-10+0*math.cos(sine/10)),math.rad(5+0*math.cos(sine/20))),.2) 
LH.C0=LH.C0:Lerp(CFrame.new(-0.5+0*math.cos(sine/10),-1+0*math.cos(sine/10),0+0*math.cos(sine/10))*CFrame.Angles(math.rad(-20+-5*math.cos(sine/20)),math.rad(10+0*math.cos(sine/10)),math.rad(-5+0*math.cos(sine/10))),.2)
elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
end
srv.RenderStepped:Wait()
end
end)()
end)

--[[
OMG!!!!!!! FUNNY!!!!!!!

I will literally die
]]--


ScriptsTab:NewButton('original sex script', 'the only reason anyone bought pendulum hub', function()
_reanimate()local a=game:GetObjects('rbxassetid://9206853840')[1]a.Parent=workspace.non;local b=a.Victim;b.Parent=workspace.non;NewInstance=function(c,d,e)local f=Instance.new(c)f.Parent=d;if e then for g,h in next,e do pcall(function()f[g]=h end)end end;return f end;function newMotor(i,j,k,l)return NewInstance('Weld',i,{Part0=i,Part1=j,C0=k,C1=l})end;a.NoNoGui.Parent=game:GetService('CoreGui')game.Players.LocalPlayer.Character.Humanoid.Died:Connect(function()game:GetService('CoreGui'):FindFirstChild('NoNoGui'):Destroy()end)local m=setmetatable({},{__index=function(n,g)return game:service(g)end})local o={N=CFrame.new,A=CFrame.Angles,fEA=CFrame.fromEulerAnglesXYZ}local p={tRGB=function(q)return q.r*255,q.g*255,q.b*255 end,N=Color3.new,RGB=Color3.fromRGB,HSV=Color3.fromHSV,tHSV=Color3.toHSV}local r={N=Vector3.new,FNI=Vector3.FromNormalId,A=Vector3.FromAxis}local s={C=math.cos,R=math.rad,S=math.sin,P=math.pi,RNG=math.random,MRS=math.randomseed,H=math.huge,RRNG=function(t,u,v)return math.rad(math.random(t,u)/(v or 1))end}local w={N=Region3.new}local x=m.Debris;local y=workspace;local z=m.Lighting;local A=m.ReplicatedStorage;local B=Instance.new;local C=m.Players;local D=game:GetService('Players').LocalPlayer;local E=workspace.non;Position=Instance.new("StringValue",E)Position.Name="Position2"Position.Value="Doggy Style"local F=D:GetMouse()local G=E:FindFirstChildOfClass'Humanoid'local H=E.Torso;local I=E["Right Arm"]local J=E["Left Arm"]local K=E["Right Leg"]local L=E["Left Leg"]local M=E:FindFirstChild'HumanoidRootPart'local N=E.Head;local O=0;local P=1;local Q=false;local R=true;local S=30;local T=true;local U=true;local b=E:WaitForChild("Victim")local Position=E.Position2.Value;local V=false;local W=false;local X=false;local Y=false;local Z=8;local _=0;local a0=16;local a1=0;E.HumanoidRootPart.Anchored=true;wsasa=newMotor(a.Position.Weld,M)Positionv=a.Position;Positionv.Parent=E;NewInstance=function(c,d,e)local f=Instance.new(c)f.Parent=d;if e then for g,h in next,e do pcall(function()f[g]=h end)end end;return f end;local a2={}local a3=b:WaitForChild'Head'local a4=b:WaitForChild'Torso'local a5=b:WaitForChild'Left Arm'local a6=b:WaitForChild'Right Arm'local a7=b:WaitForChild'Left Leg'local a8=b:WaitForChild'Right Leg'local a9=b:WaitForChild'HumanoidRootPart'wsasa.Part1=E.HumanoidRootPart;local aa=newMotor(H,N,o.N(0,1.5,0),o.N())local ab=newMotor(M,H,o.N(),o.N())local ac=newMotor(H,K,o.N(.5,-1,0),o.N(0,1,0))local ad=newMotor(H,I,o.N(1.5,.5,0),o.N(0,.5,0))local ae=newMotor(H,L,o.N(-.5,-1,0),o.N(0,1,0))local af=newMotor(H,J,o.N(-1.5,.5,0),o.N(0,.5,0))local ag=newMotor(a4,a3,o.N(0,1.5,0),o.N())local ah=newMotor(a9,a4,o.N(),o.N())local ai=newMotor(a4,a8,o.N(.5,-1,0),o.N(0,1,0))local aj=newMotor(a4,a6,o.N(1.5,.5,0),o.N(0,.5,0))local ak=newMotor(a4,a7,o.N(-.5,-1,0),o.N(0,1,0))local al=newMotor(a4,a5,o.N(-1.5,.5,0),o.N(0,.5,0))NK,RJ,RH,RS,LH,LS,NK2,RJ2,RH2,RS2,LH2,LS2=aa,ab,ac,ad,ae,af,ag,ah,ai,aj,ak,al;table.insert(a2,aa)table.insert(a2,ae)table.insert(a2,ab)table.insert(a2,ad)table.insert(a2,af)table.insert(a2,ac)table.insert(a2,ag)table.insert(a2,ak)table.insert(a2,ah)table.insert(a2,aj)table.insert(a2,al)table.insert(a2,ai)local am,an,ao,ap,aq,ar=aa.C0,ab.C0,ac.C0,ad.C0,ae.C0,af.C0;function makeMusic(as,at,S)local au=H:FindFirstChild(script.Name.."song")if not au then au=NewInstance("Sound",H,{Name=script.Name.."song",Volume=5,Pitch=at or 1,Looped=true})NewInstance("EqualizerSoundEffect",au,{HighGain=0,MidGain=2,LowGain=30})end;if as=='stop'then if au then au:Stop()end else local S=typeof(S)=='number'and S or au.TimePosition;au.Volume=5;au.Name=script.Name.."song"au.Looped=true;au.SoundId="rbxassetid://"..as;au.Pitch=at or 1;au:Play()au.TimePosition=S end;return au end;function playMusic(as,av,S)return makeMusic(as,av,S)end;for aw,h in next,G:GetPlayingAnimationTracks()do h:Stop(0)end;local ax=60;local ay=script:FindFirstChild'Heartbeat'or B("BindableEvent",script)ay.Name="Heartbeat"local az=0;local aA=true;local aB=true;local aC=tick()local aD=1/ax;ay:Fire()game:GetService("RunService").Stepped:connect(function(n,aE)az=az+n;if az>=aD then if aA then ay:Fire()aC=tick()else for g=1,math.floor(az/aD)do ay:Fire()end;aC=tick()end;if aB then az=0 else az=az-aD*math.floor(az/aD)end end end)function swait(aF)if aF==0 or aF==nil then ay.Event:wait()else for g=0,aF do ay.Event:wait()end end end;game.Players.LocalPlayer.Character.Humanoid.Died:Connect(function()ay:Destroy()end)if workspace:FindFirstChild(script.Name..'Effects')then workspace[script.Name..'Effects']:destroy()end;local aG=NewInstance("Folder",E)aG.Name=script.Name..'Effects'function ShowDamage(aH,aI,aJ,aK)local aH=aH or r.N(0,0,0)local aI=tostring(aI or"")local aJ=aJ or 2;local aK=aK or p.N(1,0,1)local aL=Part(aG,aK,Enum.Material.SmoothPlastic,r.N(.05,.05,.05),CFrame.new(aH),true,false)aL.Transparency=1;local aM=NewInstance("BillboardGui",aL,{Size=UDim2.new(3,0,3,0),Adornee=aL})local aN=NewInstance("TextLabel",aM,{BackgroundTransparency=1,Size=UDim2.new(1,0,1,0),Text=aI,TextColor3=aK,TextScaled=true,Font=Enum.Font.ArialBold})m.Debris:AddItem(aL,aJ+.5)delay(0,function()local aO=math.random(-10,10)/15;local aP=.2;local aQ=aJ/ax;for g=0,1.1,.02 do swait()aN.Rotation=aN.Rotation+aO;aP=aP-.008;aL.Position=aL.Position+Vector3.new(0,aP,0)aN.TextTransparency=g;aN.TextStrokeTransparency=g end;if aL and aL.Parent then aL:Destroy()end end)end;local aR=B("Sound")function Sound(d,as,av,aS,aT,aU,aV)local Sound=aR:Clone()Sound.SoundId="rbxassetid://"..tostring(as or 0)Sound.Pitch=av or 1;Sound.Volume=aS or 1;Sound.Looped=aT or false;if aV then coroutine.wrap(function()repeat wait()until Sound.IsLoaded;Sound.Playing=aV or false end)()end;if not aT and aU then Sound.Stopped:connect(function()Sound.Volume=0;Sound:destroy()end)elseif aU then warn("Sound can't be looped and a sound effect!")end;Sound.Parent=d or H;return Sound end;function Part(d,aW,aX,aY,aZ,a_,b0)local b1=B("Part")b1.Parent=d or E;b1[typeof(aW)=='BrickColor'and'BrickColor'or'Color']=aW or p.N(0,0,0)b1.Material=aX or Enum.Material.SmoothPlastic;b1.TopSurface,b1.BottomSurface=10,10;b1.Size=aY or r.N(1,1,1)b1.CFrame=aZ or o.N(0,0,0)b1.CanCollide=b0 or false;b1.Anchored=a_ or false;return b1 end;function Weld(b2,b3,b4,b5)local b6=B("Weld")b6.Parent=b2;b6.Part0=b2;b6.Part1=b3;b6.C0=b4 or o.N()b6.C1=b5 or o.N()return b6 end;function Mesh(d,b7,b8,b9,ba,bb)local b1=B("SpecialMesh")b1.MeshId=b8 or""b1.TextureId=b9 or""b1.Scale=ba or r.N(1,1,1)b1.Offset=bb or r.N(0,0,0)b1.MeshType=b7 or Enum.MeshType.Sphere;b1.Parent=d;return b1 end;function GotEffect(bc)local aW=bc.Color or Color3.new(.7,.7,.7)local bd=bc.EndColor or nil;local be=bc.Material or Enum.Material.SmoothPlastic;local aZ=bc.CFrame or CFrame.new()local bf=bc.EndPos or nil;local bg=bc.Mesh or{}local bh=bc.Sound or{}local aY=bc.Size or Vector3.new(1,1,1)local bi=bc.EndSize or Vector3.new(6,6,6)local bj=bc.RotInc or{0,0,0}local bk=bc.Transparency or NumberRange.new(0,1)local bl=bc.Acceleration or nil;local bm=bc.EndRotation or{0,0,0}local bn=bc.Style or false;local bo=bc.Lifetime or 1;local bp=bc.FXSystem;local m,bq;local br=Part(workspace,aW,be,Vector3.new(1,1,1),aZ,true,false)if bg=="Blast"then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://20329976','',aY,Vector3.new(0,0,-aY.X/8))elseif bg=='Ring'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://559831844','',aY,Vector3.new(0,0,0))elseif bg=='Slash1'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://662586858','',Vector3.new(aY.X/10,.001,aY.Z/10),Vector3.new(0,0,0))elseif bg=='Slash2'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://448386996','',Vector3.new(aY.X/1000,aY.Y/100,aY.Z/100),Vector3.new(0,0,0))elseif bg=='Tornado1'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://443529437','',aY/10,Vector3.new(0,0,0))elseif bg=='Tornado2'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://168892432','',aY/4,Vector3.new(0,0,0))elseif bg=='Skull'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://4770583','',aY*2,Vector3.new(0,0,0))elseif bg=='Crystal'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://9756362','',aY,Vector3.new(0,0,0))elseif bg=='Cloud'then bq=Mesh(br,Enum.MeshType.FileMesh,'rbxassetid://1095708','',aY,Vector3.new(0,0,0))elseif typeof(bg)=='table'then local bs=bg.Type or Enum.MeshType.Brick;local ID=bg.ID or''local bt=bg.Texture or''local bu=bg.Offset or Vector3.new(0,0,0)bq=Mesh(br,bs,ID,bt,aY,bu)else bq=Mesh(br,Enum.MeshType.Brick,'','',aY)end;local bv=typeof(bk)=='number'and bk or typeof(bk)=='NumberRange'and bk.Min or typeof(bk)=='table'and bk[1]or 0;local bw=typeof(bk)=='NumberRange'and bk.Max or typeof(bk)=='table'and bk[2]or 1;br.Transparency=bv;local bx=Random.new()game:service'Debris':AddItem(br,bo+3)local by=1;if bq.MeshId=='rbxassetid://20329976'then bq.Offset=Vector3.new(0,0,-bq.Scale.Z/8)elseif bq.MeshId=='rbxassetid://4770583'then by=2 elseif bq.MeshId=='rbxassetid://168892432'then by=.25 elseif bq.MeshId=='rbxassetid://443529437'then by=.1 elseif bq.MeshId=='rbxassetid://443529437'then by=.1 end;coroutine.wrap(function()if bp=='Legacy'or bp==1 or bp==nil then local bz=(typeof(bo)=='NumberRange'and bx:NextNumber(bo.Min,bo.Max)or typeof(bo)=='number'and bo or 1)*ax;for g=0,bz do local v=g/bz;br.Transparency=bv+(bw-bv)*v;bq.Scale=aY:lerp(bi*by,v)local bA=CFrame.Angles(0,0,0)if bj=='random'then bA=CFrame.Angles(math.rad(bx:NextNumber(-180,180)),math.rad(bx:NextNumber(-180,180)),math.rad(bx:NextNumber(-180,180)))elseif typeof(bj)=='table'then bA=CFrame.Angles(unpack(bj))end;if bq.MeshId=='rbxassetid://20329976'then bq.Offset=Vector3.new(0,0,-bq.Scale.Z/8)end;if bf and typeof(bf)=='CFrame'then br.CFrame=aZ:lerp(bf,v)*bA elseif bl and typeof(bl)=='table'and bl.Force then local bB=bl.Force;if typeof(bB)=='CFrame'then bB=bB.p end;if typeof(bB)=='Vector3'then if bl.LookAt then br.CFrame=(CFrame.new(br.Position,bB)+bB)*bA else br.CFrame=(br.CFrame+bB)*bA end end else br.CFrame=br.CFrame*bA end;if bd and typeof(bd)=='Color3'then br.Color=aW:lerp(bd,v)end;swait()end;br:destroy()elseif bp=='Experimental'or bp==2 then local bC=TweenInfo.new(bo,bn,Enum.EasingDirection.InOut,0,false,0)local bD=TweenInfo.new(bo,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut,0,false,0)if bn==Enum.EasingStyle.Elastic then bC=TweenInfo.new(bo*2,bn,Enum.EasingDirection.Out,0,false,0)elseif bn==Enum.EasingStyle.Bounce then bC=TweenInfo.new(bo,bn,Enum.EasingDirection.Out,0,false,0)end;local bE=game:service'TweenService':Create(br,bD,{CFrame=(typeof(bf)=='CFrame'and bf or br.CFrame)*CFrame.Angles(unpack(bm)),Color=typeof(bd)=='Color3'and bd or aW,Transparency=bw})local bF=Vector3.new(0,0,0)if bq.MeshId=='rbxassetid://20329976'then bF=Vector3.new(0,0,(bi*by).Z/8)end;local bG=game:service'TweenService':Create(bq,bC,{Scale=bi*by,Offset=bF})bE:Play()bG:Play()end end)()end;function Effect(bc)return GotEffect(bc)end;function Trail(bc)coroutine.wrap(function()bc.Frames=typeof(bc.Frames)=='number'and bc.Frames or 60;bc.CFrame=typeof(bc.CFrame)=='CFrame'and bc.CFrame or M.CFrame;local bH=typeof(bc.EndPos)=='CFrame'and bc.EndPos or bc.CFrame*CFrame.new(0,5,0)bc.EndPos=nil;local bI=Part(aG,BrickColor.new'White',Enum.Material.SmoothPlastic,r.N(.05,.05,.05),bc.CFrame,true,false)bI.Transparency=1;local bJ=bc.CFrame;for g=1,bc.Frames do bI.CFrame=bJ:lerp(bH,g/bc.Frames)bc.CFrame=bI.CFrame;Effect(bc)swait()end end)()end;local bK=E.Victim;local bL=math.random(-999999,999999)function RemovePants(bM)for g,h in pairs(bM:GetDescendants())do if h:IsA("Shirt")then h:Destroy()end end end;function RemoveShirt(bM)for g,h in pairs(bM:GetDescendants())do if h:IsA("Pants")then h:Destroy()end end end;function RemovePieces(bM)for g,h in pairs(bM:GetDescendants())do if h:IsA("Clothing")then h:Destroy()end end end;function ConnectModelToBodyPart(bN,bM,bO)local bP=bN:clone()bP.Parent=bM;local bQ=bP:GetChildren()for g=1,#bQ do if bQ[g]:IsA("BasePart")then local bR=Instance.new("Weld")bR.Part0=bP.Middle;bR.Part1=bQ[g]local bS=CFrame.new(bP.Middle.Position)bR.C0=bP.Middle.CFrame:inverse()*bS;bR.C1=bQ[g].CFrame:inverse()*bS;bR.Parent=bP.Middle end;local bT=Instance.new("Weld")bT.Part0=bO;bT.Part1=bP.Middle;bT.C0=CFrame.new(0,0,0)bT.Parent=bT.Part0 end;local bU=bP:GetChildren()for g,bV in pairs(bU)do if bV:IsA("BasePart")then bV.Anchored=false;bV.CanCollide=false;if bV.Name=="Pow"then bV.Color=bO.Color end end end;bP.Middle.Transparency=1 end;function RemoveChange(bM)if bM:FindFirstChild("ChestMesh")then bM.ChestMesh:Destroy()end;if bM:FindFirstChild("LeftArmMesh")then bM.LeftArmMesh:Destroy()end;if bM:FindFirstChild("RightArmMesh")then bM.RightArmMesh:Destroy()end;if bM:FindFirstChild("LeftLegMesh")then bM.LeftLegMesh:Destroy()end;if bM:FindFirstChild("RightLegMesh")then bM.RightLegMesh:Destroy()end;if bM:FindFirstChild("HeadMesh")then bM.HeadMesh:Destroy()end;bM.PlayerHasAChange:Destroy()end;function ChangeCharacter(bM)if true then RemovePieces(bM)end;local bW=Instance.new("IntValue")bW.Name="PlayerHasAChange"bW.Value=bL;bW.Parent=bM;if bK:FindFirstChild("ChestMesh")then ConnectModelToBodyPart(bK.ChestMesh,bM,bM["Torso"])end;if bK:FindFirstChild("LeftArmMesh")then ConnectModelToBodyPart(bK.LeftArmMesh,bM,bM["Left Arm"])end;if bK:FindFirstChild("RightArmMesh")then ConnectModelToBodyPart(bK.RightArmMesh,bM,bM["Right Arm"])end;if bK:FindFirstChild("LeftLegMesh")then ConnectModelToBodyPart(bK.LeftLegMesh,bM,bM["Left Leg"])end;if bK:FindFirstChild("RightLegMesh")then ConnectModelToBodyPart(bK.RightLegMesh,bM,bM["Right Leg"])end;if bK:FindFirstChild("HeadMesh")then ConnectModelToBodyPart(bK.HeadMesh,bM,bM["Head"])end end;local bM=b;if bM==nil then return end;if bM:findFirstChild("Humanoid")~=nil then if bM:findFirstChild("PlayerHasAChange")then if bM.PlayerHasAChange.Value~=bL then end else end end;print(NK2.Part0.Parent.Name)function ClientTrail(bc)coroutine.wrap(function()bc.Frames=typeof(bc.Frames)=='number'and bc.Frames or 60;bc.CFrame=typeof(bc.CFrame)=='CFrame'and bc.CFrame or M.CFrame;local bH=typeof(bc.EndPos)=='CFrame'and bc.EndPos or bc.CFrame*CFrame.new(0,5,0)bc.EndPos=nil;local bI=Part(aG,BrickColor.new'White',Enum.Material.SmoothPlastic,r.N(.05,.05,.05),bc.CFrame,true,false)bI.Transparency=1;local bJ=bc.CFrame;for g=1,bc.Frames do bI.CFrame=bJ:lerp(bH,g/bc.Frames)bc.CFrame=bI.CFrame;GotEffect(bc)swait()end end)()end;function syncStuff(bc)local bX,bY,bZ,b_,c0,c1,c2,c3=unpack(bc)local c4,c5,c6,c7,c8,c9,ca,cb,cc,cd,ce,cf=unpack(bZ)local cg,ch,ci,cj,ck,cl,cm,cn,co,cp,cq,cr=unpack(b_)U=bY;R=bX;if not bX then NK.C0=c4;RJ.C0=c5;RH.C0=c6;RS.C0=c7;LH.C0=c8;LS.C0=c9;NK.C1=cg;RJ.C1=ch;RH.C1=ci;RS.C1=cj;LH.C1=ck;LS.C1=cl;NK2.C0=ca;RJ2.C0=cb;RH2.C0=cc;RS2.C0=cd;LH2.C0=ce;LS2.C0=cf;NK2.C1=cm;RJ2.C1=cn;RH2.C1=co;RS2.C1=cp;LH2.C1=cq;LS2.C1=cr end;Z=c1;T=c2;P=c3;if O-c0>.8 or O-c0<-.8 then O=c0 end end;function LoopDoggyStyle()R=false;U=false;Q=true;Countt=1;game:service'UserInputService'.InputBegan:connect(function(cs,ct)if ct then return end;if cs.KeyCode==Enum.KeyCode.Z then V=false end end)repeat swait()for g=0,10 do swait()local cu=.3;RJ.C0=RJ.C0:lerp(o.N(0,-0.2,-0.6)*o.A(math.rad(10),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.3,0.1,-0.5)*o.A(math.rad(35),math.rad(0),math.rad(15)),cu)RS.C0=RS.C0:lerp(o.N(1.4,0,-0.5)*o.A(math.rad(35),math.rad(0),math.rad(-10)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(5),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-0.9,0)*o.A(math.rad(-25),math.rad(0),math.rad(0)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-0.9,0)*o.A(math.rad(-25),math.rad(0),math.rad(0)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-1.7,-0.5)*o.A(math.rad(-125),math.rad(0),math.rad(0)),cu)LS2.C0=LS2.C0:lerp(o.N(-0.9,1.3,-0.1)*o.A(math.rad(-170),math.rad(0),math.rad(40)),cu)RS2.C0=RS2.C0:lerp(o.N(1,1.5,0)*o.A(math.rad(-160),math.rad(0),math.rad(-25)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.2,0.7)*o.A(math.rad(90.3),math.rad(-19.9),math.rad(1.8)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.6,-0.8,-0.1)*o.A(math.rad(85),math.rad(0),math.rad(-5)),cu)RH2.C0=RH2.C0:lerp(o.N(0.7,-0.8,-0.1)*o.A(math.rad(85),math.rad(0),math.rad(5)),cu)end;local cv=Sound(b:WaitForChild'Torso',3099459397,math.random(1,1.8),1.1,false,nil,true)cv.TimePosition=4;Countt=Countt+1;local cw={2440889605,2440891382,2440889869,2440888376}if Countt==4 then Countt=1;ID=nil;Decision=math.random(1,4)for g,h in pairs(cw)do if g==Decision then ID=h end end;sse=Sound(b.Head,ID,1,1,false,nil,true)b.Head.CustomMouthFrownRoundedTiltedFlip.Texture="http://www.roblox.com/asset/?id=2661147529"spawn(function()repeat swait()until sse.Playing==false;b.Head.CustomMouthFrownRoundedTiltedFlip.Texture="http://www.roblox.com/asset/?id=3039452348"end)end;for g=0,10 do swait()local cu=.3;RJ.C0=RJ.C0:lerp(o.N(0,-0.1,-0.7)*o.A(math.rad(-20),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.3,0.2,-0.3)*o.A(math.rad(65),math.rad(0),math.rad(15)),cu)RS.C0=RS.C0:lerp(o.N(1.4,0.2,-0.4)*o.A(math.rad(65),math.rad(0),math.rad(-10)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(-10),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-0.9,0.1)*o.A(math.rad(20),math.rad(0),math.rad(0)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,0.1)*o.A(math.rad(20),math.rad(0),math.rad(0)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-1.7,-0.1)*o.A(math.rad(-125),math.rad(0),math.rad(0)),cu)LS2.C0=LS2.C0:lerp(o.N(-0.9,1.3,-0.1)*o.A(math.rad(-170),math.rad(0),math.rad(35)),cu)RS2.C0=RS2.C0:lerp(o.N(1,1.5,0)*o.A(math.rad(-160),math.rad(0),math.rad(-20)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.2,0.7)*o.A(math.rad(85),math.rad(-20),math.rad(0)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.6,-0.8,0)*o.A(math.rad(110),math.rad(0),math.rad(-5)),cu)RH2.C0=RH2.C0:lerp(o.N(0.7,-0.9,0)*o.A(math.rad(110),math.rad(0),math.rad(5)),cu)end until V==false;Q=false;U=true;R=true end;function LoopBlowJob()R=false;U=false;Q=true;Countt=1;game:service'UserInputService'.InputBegan:connect(function(cs,ct)if ct then return end;if cs.KeyCode==Enum.KeyCode.Z then W=false end end)repeat swait()for g=0,20 do swait()local cu=.1;RJ.C0=RJ.C0:lerp(o.N(0,0,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.4,0.4,-0.4)*o.A(math.rad(70.3),math.rad(-1.7),math.rad(19.9)),cu)RS.C0=RS.C0:lerp(o.N(1.4,0.4,-0.4)*o.A(math.rad(65.6),math.rad(3.4),math.rad(-19.7)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,-0.1)*o.A(math.rad(-20),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-1,0)*o.A(math.rad(0),math.rad(10),math.rad(0)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-1.1,0)*o.A(math.rad(-160),math.rad(0),math.rad(-180)),cu)LS2.C0=LS2.C0:lerp(o.N(-1.3,0.8,-0.2)*o.A(math.rad(114.4),math.rad(5.1),math.rad(14.1)),cu)RS2.C0=RS2.C0:lerp(o.N(1.3,0.8,-0.3)*o.A(math.rad(118.7),math.rad(-8.3),math.rad(-18.3)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.5,-1.1,-1)*o.A(math.rad(-70),math.rad(0),math.rad(-10)),cu)RH2.C0=RH2.C0:lerp(o.N(0.5,-1.1,-1)*o.A(math.rad(-70),math.rad(0),math.rad(10)),cu)end;local cv=Sound(b.Torso,2767339245,math.random(1,2),1.1,false,nil,true)cv.TimePosition=8.4;for g=0,20 do swait()local cu=.1;RJ.C0=RJ.C0:lerp(o.N(0,0,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.4,0.3,-0.5)*o.A(math.rad(55.3),math.rad(-1.7),math.rad(19.9)),cu)RS.C0=RS.C0:lerp(o.N(1.4,0.3,-0.5)*o.A(math.rad(50.6),math.rad(3.4),math.rad(-19.7)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,-0.1)*o.A(math.rad(-25),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-1,0)*o.A(math.rad(0),math.rad(10),math.rad(0)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-1.2,0.1)*o.A(math.rad(-150),math.rad(0),math.rad(-180)),cu)LS2.C0=LS2.C0:lerp(o.N(-1.3,0.4,0)*o.A(math.rad(119.4),math.rad(5.1),math.rad(14.1)),cu)RS2.C0=RS2.C0:lerp(o.N(1.3,0.4,0)*o.A(math.rad(123.7),math.rad(-8.3),math.rad(-18.3)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(-10),math.rad(0),math.rad(0)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.5,-0.8,-1.1)*o.A(math.rad(-60),math.rad(0),math.rad(-10)),cu)RH2.C0=RH2.C0:lerp(o.N(0.5,-0.8,-1.1)*o.A(math.rad(-60),math.rad(0),math.rad(10)),cu)end until W==false;Q=false;U=true;R=true end;function LoopCowGirl()R=false;U=false;Q=true;Countt=1;game:service'UserInputService'.InputBegan:connect(function(cs,ct)if ct then return end;if cs.KeyCode==Enum.KeyCode.Z then X=false end end)repeat swait()for g=0,10 do swait()local cu=.3;RJ.C0=RJ.C0:lerp(o.N(0,-2.2,-0.1)*o.A(math.rad(70),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-0.8,0.6,0.5)*o.A(math.rad(-162.9),math.rad(0),math.rad(45.2)),cu)RS.C0=RS.C0:lerp(o.N(1.2,0.6,0.6)*o.A(math.rad(14.9),math.rad(-1.3),math.rad(-164.8)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(-5),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-1,-0.1)*o.A(math.rad(15),math.rad(0),math.rad(-10)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,-0.1)*o.A(math.rad(15),math.rad(0),math.rad(5)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-0.7,0.8)*o.A(math.rad(-5),math.rad(0),math.rad(0)),cu)LS2.C0=LS2.C0:lerp(o.N(-1.3,-0.1,0)*o.A(math.rad(-15),math.rad(0),math.rad(10)),cu)RS2.C0=RS2.C0:lerp(o.N(1.3,-0.1,0)*o.A(math.rad(-15),math.rad(0),math.rad(-10)),cu)NK2.C0:lerp(o.N(0,1.5,-0.3)*o.A(math.rad(-15),math.rad(0),math.rad(0)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.7,-0.4,-0.8)*o.A(math.rad(20),math.rad(0),math.rad(-10)),cu)RH2.C0=RH2.C0:lerp(o.N(0.6,-0.5,-0.8)*o.A(math.rad(20),math.rad(0),math.rad(10)),cu)end;local cv=Sound(b:WaitForChild'Torso',3099459397,math.random(1,1.8),1.1,false,nil,true)cv.TimePosition=4;Countt=Countt+1;local cw={2440889605,2440891382,2440889869,2440888376}if Countt==4 then Countt=1;ID=nil;Decision=math.random(1,4)for g,h in pairs(cw)do if g==Decision then ID=h end end;sse=Sound(b.Head,ID,1,1,false,nil,true)b.Head.CustomMouthFrownRoundedTiltedFlip.Texture="http://www.roblox.com/asset/?id=2661147529"spawn(function()repeat swait()until sse.Playing==false;b.Head.CustomMouthFrownRoundedTiltedFlip.Texture="http://www.roblox.com/asset/?id=3039452348"end)end;for g=0,10 do swait()local cu=.3;RJ.C0=RJ.C0:lerp(o.N(0,-2.3,-0.1)*o.A(math.rad(70),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-0.8,0.6,0.4)*o.A(math.rad(-162.9),math.rad(0),math.rad(45.2)),cu)RS.C0=RS.C0:lerp(o.N(1.2,0.6,0.5)*o.A(math.rad(14.9),math.rad(-1.3),math.rad(-164.8)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-1,-0.1)*o.A(math.rad(20),math.rad(0),math.rad(-10)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,-0.1)*o.A(math.rad(20),math.rad(0),math.rad(5)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-1,0.8)*o.A(math.rad(-5),math.rad(0),math.rad(0)),cu)LS2.C0=LS2.C0:lerp(o.N(-1.3,0.2,0.1)*o.A(math.rad(-30),math.rad(0),math.rad(10)),cu)RS2.C0=RS2.C0:lerp(o.N(1.3,0.2,0.1)*o.A(math.rad(-30),math.rad(0),math.rad(-10)),cu)NK2.C0:lerp(o.N(-0.1,1.6,-0.3)*o.A(math.rad(-30),math.rad(0),math.rad(0)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.7,-0.2,-0.6)*o.A(math.rad(30),math.rad(0),math.rad(-10)),cu)RH2.C0=RH2.C0:lerp(o.N(0.6,-0.2,-0.6)*o.A(math.rad(30),math.rad(0),math.rad(10)),cu)end until X==false;Q=false;U=true;R=true end;function LoopGay()R=false;U=false;Q=true;Countt=1;game:service'UserInputService'.InputBegan:connect(function(cs,ct)if ct then return end;if cs.KeyCode==Enum.KeyCode.Z then Y=false end end)repeat swait()for g=0,10 do swait()local cu=.3;RJ.C0=RJ.C0:lerp(o.N(0,0,-1.3)*o.A(math.rad(15),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.2,0.1,-0.5)*o.A(math.rad(40),math.rad(0),math.rad(25)),cu)RS.C0=RS.C0:lerp(o.N(1.3,0.1,-0.4)*o.A(math.rad(50),math.rad(0),math.rad(-25)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,-0.1)*o.A(math.rad(-20),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-1,0.1)*o.A(math.rad(-35),math.rad(0),math.rad(-5)),cu)RH.C0=RH.C0:lerp(o.N(0.6,-1,0.1)*o.A(math.rad(-35),math.rad(0),math.rad(5)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-2,-0.8)*o.A(math.rad(0),math.rad(-89.8),math.rad(90)),cu)LS2.C0=LS2.C0:lerp(o.N(-0.8,1.2,0.1)*o.A(math.rad(85),math.rad(0.9),math.rad(-4.9)),cu)RS2.C0=RS2.C0:lerp(o.N(0.1,0.5,-0.8)*o.A(math.rad(116.2),math.rad(3.2),math.rad(-39.9)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.5,-0.2)*o.A(math.rad(-10.3),math.rad(-14.8),math.rad(-2.7)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.6,-0.9,-0.1)*o.A(math.rad(15),math.rad(0),math.rad(0)),cu)RH2.C0=RH2.C0:lerp(o.N(0.8,-0.8,0)*o.A(math.rad(-12.4),math.rad(8.5),math.rad(85.9)),cu)end;local cv=Sound(b.Torso,3099459397,math.random(1,1.8),1.1,false,nil,true)cv.TimePosition=4;Countt=Countt+1;local cw={2440889605,2440891382,2440889869,2440888376}if Countt==4 then Countt=1;ID=nil;Decision=math.random(1,4)for g,h in pairs(cw)do if g==Decision then ID=h end end;sse=Sound(b.Head,ID,1,1,false,nil,true)b.Head.CustomMouthFrownRoundedTiltedFlip.Texture="http://www.roblox.com/asset/?id=2661147529"spawn(function()repeat swait()until sse.Playing==false;b.Head.CustomMouthFrownRoundedTiltedFlip.Texture="http://www.roblox.com/asset/?id=3039452348"end)end;for g=0,10 do swait()local cu=.3;RJ.C0=RJ.C0:lerp(o.N(0,0,-0.8)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.2,0.3,-0.6)*o.A(math.rad(55),math.rad(0),math.rad(25)),cu)RS.C0=RS.C0:lerp(o.N(1.3,0.2,-0.5)*o.A(math.rad(65),math.rad(0),math.rad(-25)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,-0.1)*o.A(math.rad(-20),math.rad(0),math.rad(0)),cu)LH.C0=LH.C0:lerp(o.N(-0.5,-1,0)*o.A(math.rad(0),math.rad(0),math.rad(-5)),cu)RH.C0=RH.C0:lerp(o.N(0.6,-1,0)*o.A(math.rad(0),math.rad(0),math.rad(5)),cu)RJ2.C0=RJ2.C0:lerp(o.N(0,-2,-1.5)*o.A(math.rad(0),math.rad(-89.8),math.rad(90)),cu)LS2.C0=LS2.C0:lerp(o.N(-0.8,1.1,0.1)*o.A(math.rad(95),math.rad(0),math.rad(-5)),cu)RS2.C0=RS2.C0:lerp(o.N(0.1,0.4,-0.8)*o.A(math.rad(120),math.rad(0),math.rad(-40)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.5,-0.2)*o.A(math.rad(-10.3),math.rad(-14.8),math.rad(-2.7)),cu)LH2.C0=LH2.C0:lerp(o.N(-0.6,-0.9,-0.1)*o.A(math.rad(15),math.rad(0),math.rad(0)),cu)RH2.C0=RH2.C0:lerp(o.N(0.9,-0.9,0)*o.A(math.rad(-12.4),math.rad(8.5),math.rad(55.9)),cu)end until Y==false;Q=false;U=true;R=true end;game:service'UserInputService'.InputBegan:connect(function(cs,ct)if ct or Q then return end;if cs.KeyCode==Enum.KeyCode.Z and Q==false and Position=="Doggy Style"then V=true;LoopDoggyStyle()elseif cs.KeyCode==Enum.KeyCode.Z and Q==false and Position=="Blowjob"then W=true;LoopBlowJob()elseif cs.KeyCode==Enum.KeyCode.Z and Q==false and Position=="Cowgirl"then X=true;LoopCowGirl()elseif cs.KeyCode==Enum.KeyCode.Z and Q==false and Position=="FuckMeSidewaysAndCallMeGay"then Y=true;LoopGay()end;if cs.KeyCode==Enum.KeyCode.One and Q==false and Position~="Doggy Style"then E.Position2.Value="Doggy Style"elseif cs.KeyCode==Enum.KeyCode.Two and Q==false and Position~="Blowjob"then E.Position2.Value="Blowjob"elseif cs.KeyCode==Enum.KeyCode.Three and Q==false and Position~="Cowgirl"then E.Position2.Value="Cowgirl"elseif cs.KeyCode==Enum.KeyCode.Four and Q==false and Position~="FuckMeSidewaysAndCallMeGay"then E.Position2.Value="FuckMeSidewaysAndCallMeGay"end end)local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["SeeMonkey"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a4;a4.Transparency=1;Weld.C0=CFrame.new(0,0,0)*CFrame.Angles(math.rad(90),math.rad(0),math.rad(0))local cA=game:GetService("Workspace").non[game.Players.LocalPlayer.Name]["SeeMonkey"].Handle:FindFirstChildOfClass("SpecialMesh")cA:Destroy()local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["Pal Hair"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a5;a5.Transparency=1;Weld.C0=CFrame.new(0,0,0)*CFrame.Angles(math.rad(90),math.rad(0),math.rad(0))local cA=game:GetService("Workspace").non[game.Players.LocalPlayer.Name]["Pal Hair"].Handle:FindFirstChildOfClass("SpecialMesh")cA:Destroy()local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["LavanderHair"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a6;a6.Transparency=1;Weld.C0=CFrame.new(0,0,0)*CFrame.Angles(math.rad(90),math.rad(0),math.rad(0))local cA=game:GetService("Workspace").non[game.Players.LocalPlayer.Name]["LavanderHair"].Handle:FindFirstChildOfClass("SpecialMesh")cA:Destroy()local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["Robloxclassicred"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a7;a7.Transparency=1;Weld.C0=CFrame.new(0,0,0)*CFrame.Angles(math.rad(90),math.rad(0),math.rad(0))local cA=game:GetService("Workspace").non[game.Players.LocalPlayer.Name]["Robloxclassicred"].Handle:FindFirstChildOfClass("SpecialMesh")cA:Destroy()local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["Pink Hair"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a8;a8.Transparency=1;Weld.C0=CFrame.new(0,0,0)*CFrame.Angles(math.rad(90),math.rad(0),math.rad(0))local cA=game:GetService("Workspace").non[game.Players.LocalPlayer.Name]["Pink Hair"].Handle:FindFirstChildOfClass("SpecialMesh")cA:Destroy()local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["Space Cop"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a4;a8.Transparency=1;Weld.C0=CFrame.new(-.5,-1,.5)*CFrame.Angles(math.rad(90),math.rad(0),math.rad(0))local cA=game:GetService("Workspace").non[game.Players.LocalPlayer.Name]["Space Cop"].Handle:FindFirstChildOfClass("SpecialMesh")cA:Destroy()local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["SpaceHelmetB"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a4;a8.Transparency=1;Weld.C0=CFrame.new(.5,-1,.5)*CFrame.Angles(math.rad(90),math.rad(0),math.rad(0))local cA=game:GetService("Workspace").non[game.Players.LocalPlayer.Name]["SpaceHelmetB"].Handle:FindFirstChildOfClass("SpecialMesh")cA:Destroy()local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["Neko Idol Anime Head"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a3;a3.Transparency=1;Weld.C0=CFrame.new(0,0,0)*CFrame.Angles(math.rad(0),math.rad(0),math.rad(0))local cx=game.Players.LocalPlayer;local cy=cx.Character;local cz=cy["LooseSideBuns"].Handle;cz:BreakJoints()local Weld=Instance.new("Weld",game.Players.LocalPlayer.Character)Weld.Part1=cz;Weld.Part0=a3;Weld.C0=CFrame.new(0,-.65,.21)*CFrame.Angles(math.rad(0),math.rad(0),math.rad(0))game:GetService("Workspace").non.Victim.Head.LongHairHeadBandBrown:Destroy()local cB={[Enum.Material.Grass]=510933218,[Enum.Material.Metal]=1263161138,[Enum.Material.CorrodedMetal]=1263161138,[Enum.Material.DiamondPlate]=1263161138,[Enum.Material.Wood]=2452053757,[Enum.Material.WoodPlanks]=2452053757,[Enum.Material.Sand]=134456884,[Enum.Material.Snow]=2452051182}local cC=game['Run Service'].Heartbeat:Connect(function()b.HumanoidRootPart.CFrame=E:WaitForChild("Position",60).NewTorsoPos.CFrame;O=O+P;Position=E.Position2.Value;local cD,cE=workspace:FindPartOnRayWithIgnoreList(Ray.new(M.CFrame.p,CFrame.new(M.Position,M.Position-Vector3.new(0,1,0)).lookVector.unit*4),{aG,E})local cF=math.abs(M.Velocity.x)>1 or math.abs(M.Velocity.z)>1;local cG=G.PlatformStand and'Paralyzed'or G.Sit and'Sit'or not cD and M.Velocity.y<-1 and"Fall"or not cD and M.Velocity.y>1 and"Jump"or cD and cF and"Walk"or cD and"Idle"G.WalkSpeed=a0;local cH=math.clamp((M.Velocity*M.CFrame.rightVector).X+(M.Velocity*M.CFrame.rightVector).Z,-G.WalkSpeed,G.WalkSpeed)local cI=math.clamp((M.Velocity*M.CFrame.lookVector).X+(M.Velocity*M.CFrame.lookVector).Z,-G.WalkSpeed,G.WalkSpeed)local cJ=cH/G.WalkSpeed;local cK=cI/G.WalkSpeed;local cL,cM=workspace:FindPartOnRayWithIgnoreList(Ray.new(L.CFrame.p,CFrame.new(L.Position,L.Position-Vector3.new(0,1,0)).lookVector.unit*2),{aG,E})local cN,cO=workspace:FindPartOnRayWithIgnoreList(Ray.new(K.CFrame.p,CFrame.new(K.Position,K.Position-Vector3.new(0,1,0)).lookVector.unit*2),{aG,E})if Position=="Doggy Style"then local cu=.3;P=1;if R then RJ.C0=RJ.C0:lerp(o.N(0,-0.1,-0.7)*o.A(math.rad(-20),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.3,0.2,-0.3)*o.A(math.rad(65),math.rad(0),math.rad(15)),cu)RS.C0=RS.C0:lerp(o.N(1.4,0.2,-0.4)*o.A(math.rad(65),math.rad(0),math.rad(-10)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(-10),math.rad(0),math.rad(0)),cu)end;if U then LH.C0=LH.C0:lerp(o.N(-0.5,-0.9,0.1)*o.A(math.rad(20),math.rad(0),math.rad(0)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,0.1)*o.A(math.rad(20),math.rad(0),math.rad(0)),cu)end;if R then RJ2.C0=RJ2.C0:lerp(o.N(0,-1.7,-0.1)*o.A(math.rad(-125),math.rad(0),math.rad(0)),cu)LS2.C0=LS2.C0:lerp(o.N(-0.9,1.3,-0.1)*o.A(math.rad(-170),math.rad(0),math.rad(35)),cu)RS2.C0=RS2.C0:lerp(o.N(1,1.5,0)*o.A(math.rad(-160),math.rad(0),math.rad(-20)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.2,0.7)*o.A(math.rad(85),math.rad(-20),math.rad(0)),cu)end;if U then LH2.C0=LH2.C0:lerp(o.N(-0.6,-0.8,0)*o.A(math.rad(110),math.rad(0),math.rad(-5)),cu)RH2.C0=RH2.C0:lerp(o.N(0.7,-0.9,0)*o.A(math.rad(110),math.rad(0),math.rad(5)),cu)end elseif Position=="Blowjob"then local cu=.3;if R then RJ.C0=RJ.C0:lerp(o.N(0,0,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.4,0.4,-0.4)*o.A(math.rad(70.3),math.rad(-1.7),math.rad(19.9)),cu)RS.C0=RS.C0:lerp(o.N(1.4,0.4,-0.4)*o.A(math.rad(65.6),math.rad(3.4),math.rad(-19.7)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,-0.1)*o.A(math.rad(-20),math.rad(0),math.rad(0)),cu)end;if U then LH.C0=LH.C0:lerp(o.N(-0.5,-1,0)*o.A(math.rad(0),math.rad(10),math.rad(0)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)end;if R then RJ2.C0=RJ2.C0:lerp(o.N(0,-1.1,0)*o.A(math.rad(-160),math.rad(0),math.rad(-180)),cu)LS2.C0=LS2.C0:lerp(o.N(-1.4,0.4,-0.4)*o.A(math.rad(70.3),math.rad(-1.7),math.rad(19.9)),cu)RS2.C0=RS2.C0:lerp(o.N(1.4,0.4,-0.4)*o.A(math.rad(65.6),math.rad(3.4),math.rad(-19.7)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)end;if U then LH2.C0=LH2.C0:lerp(o.N(-0.5,-1.1,-1)*o.A(math.rad(-70),math.rad(0),math.rad(-10)),cu)RH2.C0=RH2.C0:lerp(o.N(0.5,-1.1,-1)*o.A(math.rad(-70),math.rad(0),math.rad(10)),cu)end elseif Position=="Cowgirl"then local cu=.3;if R then RJ.C0=RJ.C0:lerp(o.N(0,-2.3,-0.1)*o.A(math.rad(70),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-0.8,0.6,0.4)*o.A(math.rad(-162.9),math.rad(0),math.rad(45.2)),cu)RS.C0=RS.C0:lerp(o.N(1.2,0.6,0.5)*o.A(math.rad(14.9),math.rad(-1.3),math.rad(-164.8)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,0)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)end;if U then LH.C0=LH.C0:lerp(o.N(-0.5,-1,-0.1)*o.A(math.rad(20),math.rad(0),math.rad(-10)),cu)RH.C0=RH.C0:lerp(o.N(0.5,-1,-0.1)*o.A(math.rad(20),math.rad(0),math.rad(5)),cu)end;if R then RJ2.C0=RJ2.C0:lerp(o.N(0,-1,0.8)*o.A(math.rad(-5),math.rad(0),math.rad(0)),cu)LS2.C0=LS2.C0:lerp(o.N(-1.3,0.2,0.1)*o.A(math.rad(-30),math.rad(0),math.rad(10)),cu)RS2.C0=RS2.C0:lerp(o.N(1.3,0.2,0.1)*o.A(math.rad(-30),math.rad(0),math.rad(-10)),cu)NK2.C0=NK2.C0:lerp(o.N(-0.1,1.6,-0.3)*o.A(math.rad(-30),math.rad(0),math.rad(0)),cu)end;if U then LH2.C0=LH2.C0:lerp(o.N(-0.7,-0.2,-0.6)*o.A(math.rad(30),math.rad(0),math.rad(-10)),cu)RH2.C0=RH2.C0:lerp(o.N(0.6,-0.2,-0.6)*o.A(math.rad(30),math.rad(0),math.rad(10)),cu)end elseif Position=="FuckMeSidewaysAndCallMeGay"then local cu=.3;if R then RJ.C0=RJ.C0:lerp(o.N(0,0,-0.8)*o.A(math.rad(0),math.rad(0),math.rad(0)),cu)LS.C0=LS.C0:lerp(o.N(-1.2,0.3,-0.6)*o.A(math.rad(55),math.rad(0),math.rad(25)),cu)RS.C0=RS.C0:lerp(o.N(1.3,0.2,-0.5)*o.A(math.rad(65),math.rad(0),math.rad(-25)),cu)NK.C0=NK.C0:lerp(o.N(0,1.5,-0.1)*o.A(math.rad(-20),math.rad(0),math.rad(0)),cu)end;if U then LH.C0=LH.C0:lerp(o.N(-0.5,-1,0)*o.A(math.rad(0),math.rad(0),math.rad(-5)),cu)RH.C0=RH.C0:lerp(o.N(0.6,-1,0)*o.A(math.rad(0),math.rad(0),math.rad(5)),cu)end;if R then RJ2.C0=RJ2.C0:lerp(o.N(0,-2,-1.5)*o.A(math.rad(0),math.rad(-89.8),math.rad(90)),cu)LS2.C0=LS2.C0:lerp(o.N(-0.8,1.1,0.1)*o.A(math.rad(95),math.rad(0),math.rad(-5)),cu)RS2.C0=RS2.C0:lerp(o.N(0.1,0.4,-0.8)*o.A(math.rad(120),math.rad(0),math.rad(-40)),cu)NK2.C0=NK2.C0:lerp(o.N(0,1.5,-0.2)*o.A(math.rad(-10.3),math.rad(-14.8),math.rad(-2.7)),cu)end;if U then LH2.C0=LH2.C0:lerp(o.N(-0.6,-0.9,-0.1)*o.A(math.rad(15),math.rad(0),math.rad(0)),cu)RH2.C0=RH2.C0:lerp(o.N(0.9,-0.9,0)*o.A(math.rad(-12.4),math.rad(8.5),math.rad(55.9)),cu)end end end)game.Players.LocalPlayer.Character.Humanoid.Died:connect(function()cC:Disconnect()end)
end)
