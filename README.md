_G.HackedWalkSpeed = 100

local Plrs = game:GetService("Players")

local MyPlr = Plrs.LocalPlayer
local MyChar = MyPlr.Character

if MyChar then
local Hum = MyChar.Humanoid
Hum.Changed:connect(function()
Hum.WalkSpeed = _G.HackedWalkSpeed
end)
Hum.WalkSpeed = _G.HackedWalkSpeed
end


MyPlr.CharacterAdded:connect(function(Char)
MyChar = Char
repeat wait() until Char:FindFirstChild("Humanoid")
local Hum = Char.Humanoid
Hum.Changed:connect(function()
Hum.WalkSpeed = _G.HackedWalkSpeed
end)
Hum.WalkSpeed = _G.HackedWalkSpeed
end)
local plr = game.Players.LocalPlayer
local gui = plr.PlayerGui
local ulttext = gui.ScreenGui.MagicHealth.TextLabel

ulttext.Text = "CYBER PSYCHO"

local windtrail2 = game.ReplicatedStorage.Resources.HeadFirst["CharFX"].WindTrail:Clone()
windtrail2.Parent = game.Players.LocalPlayer.Character["Right Arm"]
    for _, child in ipairs(windtrail2:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(20) -- Emit 20 particles
        end
    end

local windtrail2 = game.ReplicatedStorage.Resources.HeadFirst["CharFX"].WindTrail:Clone()
windtrail2.Parent = game.Players.LocalPlayer.Character["Left Arm"]
    for _, child in ipairs(windtrail2:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(20) -- Emit 20 particles
        end
    end

local windtrail2 = game.ReplicatedStorage.Resources.HeadFirst["CharFX"].WindTrail:Clone()
windtrail2.Parent = game.Players.LocalPlayer.Character["Right Leg"]
    for _, child in ipairs(windtrail2:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(20) -- Emit 20 particles
        end
    end

local windtrail2 = game.ReplicatedStorage.Resources.HeadFirst["CharFX"].WindTrail:Clone()
windtrail2.Parent = game.Players.LocalPlayer.Character["Left Leg"]
    for _, child in ipairs(windtrail2:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(20) -- Emit 20 particles
        end
    end

local spin1 = game.ReplicatedStorage.Resources.WhirlwindDrop["CharFX"].Spin:Clone()
spin1.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(spin1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(1) -- Emit 20 particles
        end
    end
local wow1 = game.ReplicatedStorage.Resources.Dragon["Complete"].Part.Debri:Clone()
wow1.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(wow1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(1) -- Emit 20 particles
        end
    end
local wind1 = game.ReplicatedStorage.Resources.Dragon["Stretch"].Part.Attachment:Clone()
wind1.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(wind1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(1) -- Emit 20 particles
        end
    end

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

-- Wait for the player to load
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Find the "Right Arm" part inside the player's character
local rightArm = character:WaitForChild("Right Arm")
if not rightArm then
    error("Right Arm part not found in player character")
end

-- Check for Resources folder in ReplicatedStorage
local resourcesFolder = ReplicatedStorage:WaitForChild("Resources")

-- Check for KJEffects folder inside Resources
local vanishingKickFolder = resourcesFolder:WaitForChild("VanishingKick")

-- Check for speedlinesandstuff part inside KJEffects
local speedlinesandstuffPart = vanishingKickFolder:WaitForChild("Trail2")

-- Duplicate the speedlinesandstuff part
local speedlinesandstuffClone = speedlinesandstuffPart:Clone()

-- Put the duplicate in Workspace
speedlinesandstuffClone.Parent = Workspace

-- Set the position to the Right Arm initially
speedlinesandstuffClone.CFrame = rightArm.CFrame

-- Function to enable all ParticleEmitters
local function enableParticleEmitters(parent)
    for _, descendant in ipairs(parent:GetDescendants()) do
        if descendant:IsA("ParticleEmitter") then
            descendant.Enabled = true
        end
    end
end

-- Update the clone's position every frame
RunService.RenderStepped:Connect(function()
    if character and rightArm then
        speedlinesandstuffClone.CFrame = rightArm.CFrame
    end
end)

-- Example usage after your dash effect completes
spawn(function()
    -- Simulating end of dash effect
    wait(0)  -- Adjust the wait time as needed

    -- Enable all ParticleEmitters inside speedlinesandstuffClone
    enableParticleEmitters(speedlinesandstuffClone)
end)

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

-- Wait for the player to load
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Find the "Right Arm" part inside the player's character
local rightArm = character:WaitForChild("Left Arm")
if not rightArm then
    error("Right Arm part not found in player character")
end

-- Check for Resources folder in ReplicatedStorage
local resourcesFolder = ReplicatedStorage:WaitForChild("Resources")

-- Check for KJEffects folder inside Resources
local vanishingKickFolder = resourcesFolder:WaitForChild("VanishingKick")

-- Check for speedlinesandstuff part inside KJEffects
local speedlinesandstuffPart = vanishingKickFolder:WaitForChild("Trail2")

-- Duplicate the speedlinesandstuff part
local speedlinesandstuffClone = speedlinesandstuffPart:Clone()

-- Put the duplicate in Workspace
speedlinesandstuffClone.Parent = Workspace

-- Set the position to the Right Arm initially
speedlinesandstuffClone.CFrame = rightArm.CFrame

-- Function to enable all ParticleEmitters
local function enableParticleEmitters(parent)
    for _, descendant in ipairs(parent:GetDescendants()) do
        if descendant:IsA("ParticleEmitter") then
            descendant.Enabled = true
        end
    end
end

-- Update the clone's position every frame
RunService.RenderStepped:Connect(function()
    if character and rightArm then
        speedlinesandstuffClone.CFrame = rightArm.CFrame
    end
end)

-- Example usage after your dash effect completes
spawn(function()
    -- Simulating end of dash effect
    wait(0)  -- Adjust the wait time as needed

    -- Enable all ParticleEmitters inside speedlinesandstuffClone
    enableParticleEmitters(speedlinesandstuffClone)
end)

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

-- Wait for the player to load
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Find the "Right Arm" part inside the player's character
local rightArm = character:WaitForChild("Right Leg")
if not rightArm then
    error("Right Arm part not found in player character")
end

-- Check for Resources folder in ReplicatedStorage
local resourcesFolder = ReplicatedStorage:WaitForChild("Resources")

-- Check for KJEffects folder inside Resources
local vanishingKickFolder = resourcesFolder:WaitForChild("VanishingKick")

-- Check for speedlinesandstuff part inside KJEffects
local speedlinesandstuffPart = vanishingKickFolder:WaitForChild("Trail2")

-- Duplicate the speedlinesandstuff part
local speedlinesandstuffClone = speedlinesandstuffPart:Clone()

-- Put the duplicate in Workspace
speedlinesandstuffClone.Parent = Workspace

-- Set the position to the Right Arm initially
speedlinesandstuffClone.CFrame = rightArm.CFrame

-- Function to enable all ParticleEmitters
local function enableParticleEmitters(parent)
    for _, descendant in ipairs(parent:GetDescendants()) do
        if descendant:IsA("ParticleEmitter") then
            descendant.Enabled = true
        end
    end
end

-- Update the clone's position every frame
RunService.RenderStepped:Connect(function()
    if character and rightArm then
        speedlinesandstuffClone.CFrame = rightArm.CFrame
    end
end)

-- Example usage after your dash effect completes
spawn(function()
    -- Simulating end of dash effect
    wait(0)  -- Adjust the wait time as needed

    -- Enable all ParticleEmitters inside speedlinesandstuffClone
    enableParticleEmitters(speedlinesandstuffClone)
end)

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

-- Wait for the player to load
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Find the "Right Arm" part inside the player's character
local rightArm = character:WaitForChild("Left Leg")
if not rightArm then
    error("Right Arm part not found in player character")
end

-- Check for Resources folder in ReplicatedStorage
local resourcesFolder = ReplicatedStorage:WaitForChild("Resources")

-- Check for KJEffects folder inside Resources
local vanishingKickFolder = resourcesFolder:WaitForChild("VanishingKick")

-- Check for speedlinesandstuff part inside KJEffects
local speedlinesandstuffPart = vanishingKickFolder:WaitForChild("Trail2")

-- Duplicate the speedlinesandstuff part
local speedlinesandstuffClone = speedlinesandstuffPart:Clone()

-- Put the duplicate in Workspace
speedlinesandstuffClone.Parent = Workspace

-- Set the position to the Right Arm initially
speedlinesandstuffClone.CFrame = rightArm.CFrame

-- Function to enable all ParticleEmitters
local function enableParticleEmitters(parent)
    for _, descendant in ipairs(parent:GetDescendants()) do
        if descendant:IsA("ParticleEmitter") then
            descendant.Enabled = true
        end
    end
end

-- Update the clone's position every frame
RunService.RenderStepped:Connect(function()
    if character and rightArm then
        speedlinesandstuffClone.CFrame = rightArm.CFrame
    end
end)

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:WaitForChild("Animator")

local animationId = "rbxassetid://18897115785"
local animation = Instance.new("Animation")
animation.AnimationId = animationId

local animationTrack
local isMoving = false

local function playAnimation()
    if not animationTrack then
        animationTrack = animator:LoadAnimation(animation)
    end
    
    if not isMoving then
        isMoving = true
        animationTrack:Play()
    end
end

local function stopAnimation()
    if isMoving and animationTrack then
        isMoving = false
        animationTrack:Stop()
    end
end

local function onHumanoidChanged()
    if humanoid.MoveDirection.Magnitude > 0 then
        playAnimation()
    else
        stopAnimation()
    end
end

humanoid:GetPropertyChangedSignal("MoveDirection"):Connect(onHumanoidChanged)

-- Initial check
onHumanoidChanged()

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:WaitForChild("Animator")

local animationId = "rbxassetid://18897115785"
local animation = Instance.new("Animation")
animation.AnimationId = animationId

local animationTrack
local isMoving = false

local function playAnimation()
    if not animationTrack then
        animationTrack = animator:LoadAnimation(animation)
    end
    
    if not isMoving then
        isMoving = true
        animationTrack:Play()
    end
end

local function stopAnimation()
    if isMoving and animationTrack then
        isMoving = false
        animationTrack:Stop()
    end
end

local function onHumanoidChanged()
    if humanoid.MoveDirection.Magnitude > 0 then
        playAnimation()
    else
        stopAnimation()
    end
end

humanoid:GetPropertyChangedSignal("MoveDirection"):Connect(onHumanoidChanged)

-- Initial check
onHumanoidChanged()

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:WaitForChild("Animator")

local animationId = "rbxassetid://18897115785"
local animation = Instance.new("Animation")
animation.AnimationId = animationId

local animationTrack
local isMoving = false

local function playAnimation()
    if not animationTrack then
        animationTrack = animator:LoadAnimation(animation)
    end
    
    if not isMoving then
        isMoving = true
        animationTrack:Play()
    end
end

local function stopAnimation()
    if isMoving and animationTrack then
        isMoving = false
        animationTrack:Stop()
    end
end

local function onHumanoidChanged()
    if humanoid.MoveDirection.Magnitude > 0 then
        playAnimation()
    else
        stopAnimation()
    end
end

humanoid:GetPropertyChangedSignal("MoveDirection"):Connect(onHumanoidChanged)

-- Initial check
onHumanoidChanged()

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:WaitForChild("Animator")

local animationId = "rbxassetid://18897115785"
local animation = Instance.new("Animation")
animation.AnimationId = animationId

local animationTrack
local isMoving = false

local function playAnimation()
    if not animationTrack then
        animationTrack = animator:LoadAnimation(animation)
    end
    
    if not isMoving then
        isMoving = true
        animationTrack:Play()
    end
end

local function stopAnimation()
    if isMoving and animationTrack then
        isMoving = false
        animationTrack:Stop()
    end
end

local function onHumanoidChanged()
    if humanoid.MoveDirection.Magnitude > 0 then
        playAnimation()
    else
        stopAnimation()
    end
end

humanoid:GetPropertyChangedSignal("MoveDirection"):Connect(onHumanoidChanged)

-- Initial check
onHumanoidChanged()

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:WaitForChild("Animator")

local animationId = "rbxassetid://18897115785"
local animation = Instance.new("Animation")
animation.AnimationId = animationId

local animationTrack
local isMoving = false

local function playAnimation()
    if not animationTrack then
        animationTrack = animator:LoadAnimation(animation)
    end
    
    if not isMoving then
        isMoving = true
        animationTrack:Play()
    end
end

local function stopAnimation()
    if isMoving and animationTrack then
        isMoving = false
        animationTrack:Stop()
    end
end

local function onHumanoidChanged()
    if humanoid.MoveDirection.Magnitude > 0 then
        playAnimation()
    else
        stopAnimation()
    end
end

humanoid:GetPropertyChangedSignal("MoveDirection"):Connect(onHumanoidChanged)

-- Initial check
onHumanoidChanged()

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:WaitForChild("Animator")

local animationId = "rbxassetid://18897115785"
local animation = Instance.new("Animation")
animation.AnimationId = animationId

local animationTrack
local isMoving = false

local function playAnimation()
    if not animationTrack then
        animationTrack = animator:LoadAnimation(animation)
    end
    
    if not isMoving then
        isMoving = true
        animationTrack:Play()
    end
end

local function stopAnimation()
    if isMoving and animationTrack then
        isMoving = false
        animationTrack:Stop()
    end
end

local function onHumanoidChanged()
    if humanoid.MoveDirection.Magnitude > 0 then
        playAnimation()
    else
        stopAnimation()
    end
end

humanoid:GetPropertyChangedSignal("MoveDirection"):Connect(onHumanoidChanged)

-- Initial check
onHumanoidChanged()

local function addTrailToCharacter(character)
    local leftArm = character:FindFirstChild("Left Arm") or character:FindFirstChild("LeftHand")
    local rightArm = character:FindFirstChild("Right Arm") or character:FindFirstChild("RightHand")

    if not leftArm or not rightArm then
        return
    end

    local trail = Instance.new("Trail")
    trail.Color = ColorSequence.new(Color3.new(0, 0, 1), Color3.new(0, 1, 1))
    trail.Transparency = NumberSequence.new(0, 1)
    trail.Lifetime = 1
    trail.LightEmission = 1
    trail.Attachment0 = Instance.new("Attachment", leftArm)
    trail.Attachment1 = Instance.new("Attachment", rightArm)
    trail.Parent = character
end

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

addTrailToCharacter(character)

local tool = Instance.new("Tool")
tool.Name = "Overdrive"
tool.RequiresHandle = false
tool.ToolTip = "ooh kick yes yes baby"
 
tool.Parent = game.Players.LocalPlayer.Backpack
 
local function onActivated()
  loadstring(game:HttpGet("https://pastebin.com/raw/FrGmJDSk"))()
end
 
tool.Activated:Connect(onActivated)

tool.Parent = game.Players.LocalPlayer.Backpack

local tool = Instance.new("Tool")
tool.Name = "Exiled Dash"
tool.RequiresHandle = false
tool.ToolTip = "ooh kick yes yes baby"
 
tool.Parent = game.Players.LocalPlayer.Backpack
 
local function onActivated()
  loadstring(game:HttpGet("https://pastebin.com/raw/NS3kWW3B"))()
end
 
tool.Activated:Connect(onActivated)

tool.Parent = game.Players.LocalPlayer.Backpack

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

local animationIdsToStop = {
    [13532562418] = true,
    [13532600125] = true,
    [13532604085] = true,
    [13294471966] = true,
}

local replacementAnimations = {
    [13532562418] = "rbxassetid://17889458563",
    [13532600125] = "rbxassetid://17889461810",
    [13532604085] = "rbxassetid://17889471098",
    [13294471966] = "rbxassetid://17889290569",
}

local queue = {}
local isAnimating = false

local function playReplacementAnimation(animationId)
    if isAnimating then
        table.insert(queue, animationId)
        return
    end

    isAnimating = true
    local replacementAnimationId = replacementAnimations[animationId]
    
    if replacementAnimationId then
        local animAnim = Instance.new("Animation")
        animAnim.AnimationId = replacementAnimationId
        local anim = humanoid:LoadAnimation(animAnim)
        anim:Play()

        anim.Stopped:Connect(function()
            isAnimating = false
            if #queue > 0 then
                local nextAnimationId = table.remove(queue, 1)
                playReplacementAnimation(nextAnimationId)
            end
        end)
    else
        isAnimating = false
    end
end

local function stopSpecificAnimations()
    for _, track in ipairs(humanoid:GetPlayingAnimationTracks()) do
        local animationId = tonumber(track.Animation.AnimationId:match("%d+"))
        if animationIdsToStop[animationId] then
            track:Stop()
        end
    end
end

local function onAnimationPlayed(animationTrack)
    local animationId = tonumber(animationTrack.Animation.AnimationId:match("%d+"))
    if animationIdsToStop[animationId] then
        stopSpecificAnimations()
        animationTrack:Stop()

        local replacementAnimationId = replacementAnimations[animationId]
        if replacementAnimationId then
            playReplacementAnimation(animationId)
        end
    end
end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)

local function onBodyVelocityAdded(bodyVelocity)
    if bodyVelocity:IsA("BodyVelocity") then
        bodyVelocity.Velocity = Vector3.new(bodyVelocity.Velocity.X, 0, bodyVelocity.Velocity.Z)
    end
end

character.DescendantAdded:Connect(onBodyVelocityAdded)

for _, descendant in pairs(character:GetDescendants()) do
    onBodyVelocityAdded(descendant)
end

player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    humanoid = character:WaitForChild("Humanoid")
    
    character.DescendantAdded:Connect(onBodyVelocityAdded)

    for _, descendant in pairs(character:GetDescendants()) do
        onBodyVelocityAdded(descendant)
    end
end)

game.Players.LocalPlayer.Character.Humanoid.JumpPower = 100 -- change it

local Player = game.Players.LocalPlayer
local PlayerGui = Player:WaitForChild("PlayerGui")
local ScreenGui = Instance.new("ScreenGui", PlayerGui)

-- Create the first image button
local imageButton1 = Instance.new("ImageButton")
imageButton1.Size = UDim2.new(0, 50, 0, 50)
imageButton1.Position = UDim2.new(0.5, 250, 0.5, -25) -- Adjusted to be left of the jump button
imageButton1.Image = "rbxassetid://14488863746"
imageButton1.BackgroundTransparency = 1
imageButton1.Parent = ScreenGui

-- Create the second image button
local imageButton2 = Instance.new("ImageButton")
imageButton2.Size = UDim2.new(0, 50, 0, 50)
imageButton2.Position = UDim2.new(0.5, 250, 0.5, -25) -- Adjusted to be right of the first image button
imageButton2.Image = "rbxassetid://6256840888"
imageButton2.BackgroundTransparency = 1
imageButton2.Parent = ScreenGui

-- Functionality for the first image button
imageButton1.MouseButton1Click:Connect(function()
local player = game.Players.LocalPlayer
repeat wait() until player.Character.Humanoid
local humanoid = player.Character.Humanoid
local character = player.Character or player.CharacterAdded:Wait()
local UserInputService = game:GetService("UserInputService")

-- Load animations
local anim4 = Instance.new("Animation")
anim4.AnimationId = "rbxassetid://18897119503"
local playAnim4 = humanoid:LoadAnimation(anim4)
playAnim4:Play()

local soundeffect = Instance.new("Sound")
soundeffect.SoundId = "rbxassetid://18871106251"
soundeffect.Parent = game.Players.LocalPlayer.Character.Torso
soundeffect:Play()
soundeffect.Volume = 1
wait(0.6)

local anim = Instance.new("Animation")
anim.AnimationId = "rbxassetid://18897116845"
local playAnim = humanoid:LoadAnimation(anim)
playAnim:Play()

local soundeffect = Instance.new("Sound")
soundeffect.SoundId = "rbxassetid://18871224865"
soundeffect.Parent = game.Players.LocalPlayer.Character.Torso
soundeffect:Play()
soundeffect.Volume = 1

local p = game.Players.LocalPlayer
local c = p.Character or p.CharacterAdded:Wait()
local hrp = c:WaitForChild("HumanoidRootPart")
local rs = game:GetService("ReplicatedStorage")
local ws = game:GetService("Workspace")

local r = rs.Resources
local k = r.KJEffects
local s = k.speedlinesandstuff

local t = ws:FindFirstChild("Thrown") or Instance.new("Folder", ws)
t.Name = "Thrown"

local n = s:Clone()
n.Parent = t
n.Anchored = false
n.CFrame = hrp.CFrame + Vector3.new(0, 15, 0) + hrp.CFrame.LookVector * 167

local w = Instance.new("WeldConstraint")
w.Part0 = n
w.Part1 = hrp
w.Parent = n

for _, descendant in ipairs(n:GetDescendants()) do
    if descendant:IsA("ParticleEmitter") then
        descendant.Rate = 101020228
    end
end

local sp = s:FindFirstChild("thespeedthingunderultik")
if sp then
    local d = sp:Clone()
    d.Parent = t
    d.Anchored = false
    d.CFrame = hrp.CFrame

    local wl = Instance.new("WeldConstraint")
    wl.Part0 = d
    wl.Part1 = hrp
    wl.Parent = d

    for _, descendant in ipairs(d:GetDescendants()) do
        if descendant:IsA("ParticleEmitter") then
            descendant.Rate = 1010192929292939
        end
    end
end

-- Function to destroy everything after 1 second
task.delay(1, function()
    if n then
        n:Destroy()  -- Destroy the cloned speedlinesandstuff
    end

    if t then
        t:Destroy()  -- Destroy the Thrown folder
    end

    -- Destroy other effects, if any
    for _, obj in ipairs(ws:GetChildren()) do
        if obj:IsA("Folder") and obj.Name == "Thrown" then
            obj:Destroy()
        end
        -- Add more conditions here if needed to destroy other specific objects
    end
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

-- Function to make the player walk forward in the direction they are looking
local function walkForwardByFiveFeet()
    -- Set the Humanoid's WalkSpeed to 13
    local oldWalkSpeed = humanoid.WalkSpeed
    humanoid.WalkSpeed = 500

    -- Get the current position and look vector
    local currentPosition = humanoidRootPart.Position
    local forwardVector = humanoidRootPart.CFrame.LookVector * (20 * 4.3048) -- 5 feet converted to meters
    local targetPosition = currentPosition + forwardVector

    -- Use Humanoid to move to the target position
    humanoid:MoveTo(targetPosition)

    -- Optionally, wait for the move to complete
    humanoid.MoveToFinished:Wait()

    -- Reset the Humanoid's WalkSpeed to its original value
    humanoid.WalkSpeed = oldWalkSpeed
end

-- Call the function to make the player walk forward in the direction they are looking
walkForwardByFiveFeet()
    print("Image Button 1 clicked - custom action executed")
end)

-- Functionality for the second image button
imageButton2.MouseButton1Click:Connect(function()
message = "You Tired Yet?"
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(message, "All")

local players = game:GetService("Players")
local erm = players.LocalPlayer
local bar = erm.PlayerGui.ScreenGui.MagicHealth.Health.Bar.Bar
bar.ImageColor3 = Color3.fromRGB(255, 255, 0)

local player = game.Players.LocalPlayer
repeat wait() until player.Character.Humanoid
local humanoid = player.Character.Humanoid
local character = player.Character or player.CharacterAdded:Wait()
local UserInputService = game:GetService("UserInputService")

-- Load animations
local anim4 = Instance.new("Animation")
anim4.AnimationId = "rbxassetid://18897119503"
local playAnim4 = humanoid:LoadAnimation(anim4)
playAnim4:Play()

local soundeffect = Instance.new("Sound")
soundeffect.SoundId = "rbxassetid://18871106251"
soundeffect.Parent = game.Players.LocalPlayer.Character.Torso
soundeffect:Play()
soundeffect.Volume = 1
wait(0.6)

local anim = Instance.new("Animation")
anim.AnimationId = "rbxassetid://18897116845"
local playAnim = humanoid:LoadAnimation(anim)
playAnim:Play()

local soundeffect = Instance.new("Sound")
soundeffect.SoundId = "rbxassetid://18871224865"
soundeffect.Parent = game.Players.LocalPlayer.Character.Torso
soundeffect:Play()
soundeffect.Volume = 1

local p = game.Players.LocalPlayer
local c = p.Character or p.CharacterAdded:Wait()
local hrp = c:WaitForChild("HumanoidRootPart")
local rs = game:GetService("ReplicatedStorage")
local ws = game:GetService("Workspace")

local r = rs.Resources
local k = r.KJEffects
local s = k.speedlinesandstuff

local t = ws:FindFirstChild("Thrown") or Instance.new("Folder", ws)
t.Name = "Thrown"

local n = s:Clone()
n.Parent = t
n.Anchored = false
n.CFrame = hrp.CFrame + Vector3.new(0, 15, 0) + hrp.CFrame.LookVector * 167

local w = Instance.new("WeldConstraint")
w.Part0 = n
w.Part1 = hrp
w.Parent = n

for _, descendant in ipairs(n:GetDescendants()) do
    if descendant:IsA("ParticleEmitter") then
        descendant.Rate = 101020228
    end
end

local sp = s:FindFirstChild("thespeedthingunderultik")
if sp then
    local d = sp:Clone()
    d.Parent = t
    d.Anchored = false
    d.CFrame = hrp.CFrame

    local wl = Instance.new("WeldConstraint")
    wl.Part0 = d
    wl.Part1 = hrp
    wl.Parent = d

    for _, descendant in ipairs(d:GetDescendants()) do
        if descendant:IsA("ParticleEmitter") then
            descendant.Rate = 1010192929292939
        end
    end
end

-- Function to destroy everything after 1 second
task.delay(1, function()
    if n then
        n:Destroy()  -- Destroy the cloned speedlinesandstuff
    end

    if t then
        t:Destroy()  -- Destroy the Thrown folder
    end

    -- Destroy other effects, if any
    for _, obj in ipairs(ws:GetChildren()) do
        if obj:IsA("Folder") and obj.Name == "Thrown" then
            obj:Destroy()
        end
        -- Add more conditions here if needed to destroy other specific objects
    end
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

-- Function to make the player walk forward in the direction they are looking
local function walkForwardByFiveFeet()
    -- Set the Humanoid's WalkSpeed to 13
    local oldWalkSpeed = humanoid.WalkSpeed
    humanoid.WalkSpeed = 500

    -- Get the current position and look vector
    local currentPosition = humanoidRootPart.Position
    local forwardVector = humanoidRootPart.CFrame.LookVector * (20 * 4.3048) -- 5 feet converted to meters
    local targetPosition = currentPosition + forwardVector

    -- Use Humanoid to move to the target position
    humanoid:MoveTo(targetPosition)

    -- Optionally, wait for the move to complete
    humanoid.MoveToFinished:Wait()

    -- Reset the Humanoid's WalkSpeed to its original value
    humanoid.WalkSpeed = oldWalkSpeed
end

-- Call the function to make the player walk forward in the direction they are looking
walkForwardByFiveFeet()
    print("Image Button 2 clicked - custom action executed")
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "12342141464"
local newAnimID = "18181589384"

-- Function to create an image with fade and move effects
message = "You're Not Ready For This One!"
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(message, "All")

local function createImage(assetId, position)
    local playerGui = player:WaitForChild("PlayerGui")
    local screenGui = playerGui:FindFirstChild("ScreenGui") or Instance.new("ScreenGui", playerGui)

    -- Create a Frame for the image
    local frame = Instance.new("Frame")
    frame.Size = UDim2.new(0, 70, 0, 70) -- Set size as needed
    frame.Position = position
    frame.BackgroundTransparency = 1 -- Make it transparent

    -- Create an ImageLabel for the image
    local image = Instance.new("ImageLabel", frame)
    image.Size = UDim2.new(1, 0, 1, 0)
    image.Image = "rbxassetid://" .. assetId

    -- Add the frame to the ScreenGui
    frame.Parent = screenGui

    -- Tweening to move down and fade out
    local tweenService = game:GetService("TweenService")
    local moveDown = UDim2.new(position.X.Scale, position.X.Offset, position.Y.Scale + 0.1, position.Y.Offset)

    local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Sine, Enum.EasingDirection.Out)
    local tweenMove = tweenService:Create(frame, tweenInfo, {Position = moveDown})
    local tweenFade = tweenService:Create(image, tweenInfo, {BackgroundTransparency = 1})

    tweenMove:Play()
    tweenFade:Play()

    tweenMove.Completed:Connect(function()
        frame:Destroy() -- Clean up after animation
    end)
end

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Create images after the animation is replaced
            createImage("93849000272981", UDim2.new(0, 280, 0.5, -50)) -- Left image
            createImage("107742899109645", UDim2.new(1, -350, 0.5, -50)) -- Right image

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "12351854556"
local newAnimID = "17861844708"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "12272894215"
local newAnimID = "17889458563"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "12273188754"
local newAnimID = "17799224866"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "12296113986"
local newAnimID = "18182425133"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "13630786846"
local newAnimID = "17838006839"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "13630786846"
local newAnimID = "12447247483"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

 local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "13716964686"
local newAnimID = "17292549897"
local soundEffectId = "rbxassetid://17292555531"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Play the sound effect
            local soundEffect = Instance.new("Sound")
            soundEffect.SoundId = soundEffectId
            soundEffect.Parent = character:WaitForChild("Torso")
            soundEffect.Volume = 1
            soundEffect:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local TweenService = game:GetService("TweenService")

-- Define the target and replacement animation IDs
local oldAnimID = "16310343179"
local newAnimID = "18903642853"

-- Sound IDs
local soundIds = {
    "15865495323",
    "18846960753",
    "18846960425"
}

-- Function to play a sound
local function playSound(soundId)
    local sound = Instance.new("Sound")
    sound.SoundId = "rbxassetid://" .. soundId
    sound.Volume = 5
    sound.Parent = character
    sound:Play()

    sound.Ended:Connect(function()
        sound:Destroy()
    end)
end

-- Function to play both sounds sequentially
local function playSoundsSequentially()
    playSound(soundIds[1])
    
    local sound2 = Instance.new("Sound")
    sound2.SoundId = "rbxassetid://" .. soundIds[2]
    sound2.Volume = 5
    sound2.Parent = character

    sound2.Ended:Connect(function()
        sound2:Destroy()
    end)

    sound2:Play()
    wait(sound2.TimeLength + 1.2)

    local sound3 = Instance.new("Sound")
    sound3.SoundId = "rbxassetid://" .. soundIds[3]
    sound3.Volume = 5
    sound3.Parent = character

    sound3.Ended:Connect(function()
        sound3:Destroy()
    end)

    sound3:Play()
end

-- Function to create particle effects
local function createParticleEffect()
    local ReplicatedStorage = game:GetService("ReplicatedStorage")
    local head = character:FindFirstChild("Head")
    local torso = character:FindFirstChild("Torso")

    if head and torso then
        local final1 = ReplicatedStorage.Resources.Sorcerer["WallFX"].Final.At:Clone()
        final1.Parent = head
        for _, child in ipairs(final1:GetChildren()) do
            if child:IsA("ParticleEmitter") then
                child:Emit(1)
            end
        end

        local final4 = ReplicatedStorage.Resources.Sorcerer["WallFX"].Final.Attachment:Clone()
        final4.Parent = torso
        for _, child in ipairs(final4:GetChildren()) do
            if child:IsA("ParticleEmitter") then
                child:Emit(3)
            end
        end
    end
end

-- Function to execute additional effects immediately after animation replacement
local function executeAdditionalEffects()
    local wallFX = game.ReplicatedStorage.Resources.Sorcerer.WallFX:Clone()
    wallFX:PivotTo(workspace.Live["Weakest Dummy"].HumanoidRootPart.CFrame * CFrame.new(0, 0, 1))
    wallFX.Parent = workspace.Thrown

    local barrier = game.ReplicatedStorage.Resources.Sorcerer.LimitlessBarrier:Clone()
    barrier:PivotTo(character.HumanoidRootPart.CFrame)
    barrier.Parent = workspace.Thrown

    task.delay(10, function()
        barrier:Destroy()
    end)

    local sphere = barrier.Sphere

    -- Emit particles after a short delay
    task.delay(0, function()
        for _, child in ipairs(wallFX.FirstSlam:GetChildren()) do
            if child:IsA("ParticleEmitter") then
                child:Emit(child:GetAttribute("EmitCount")) 
            end
        end
    end)

    task.delay(0.2, function()
        local colorCorrection = Instance.new("ColorCorrectionEffect")
        colorCorrection.Name = "cloned"
        colorCorrection.Parent = game.Lighting

        local barrierScreen = game.ReplicatedStorage.Resources.Sorcerer.Lighting.BarrierScreen

        TweenService:Create(colorCorrection, TweenInfo.new(0.35, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {
            Brightness = barrierScreen.Brightness,
            Contrast = barrierScreen.Contrast,
            Saturation = barrierScreen.Saturation,
            TintColor = barrierScreen.TintColor
        }):Play()

        task.wait(0.2)

        TweenService:Create(colorCorrection, TweenInfo.new(0.6, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut), {
            Brightness = 0,
            Contrast = 0,
            Saturation = 0
        }):Play()

        task.wait(0.3)
        colorCorrection:Destroy()
    end)

    task.delay(0.8, function()
        for _, child in ipairs(barrier.Core.EndEmit:GetChildren()) do
            if child:IsA("ParticleEmitter") then
                child:Emit(child:GetAttribute("EmitCount")) 
            end
        end

        for _, child in ipairs(wallFX.Final:GetChildren()) do
            if child:IsA("ParticleEmitter") then
                child:Emit(child:GetAttribute("EmitCount")) 
            end
        end
    end)
end

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    humanoid.AnimationPlayed:Connect(function(animationTrack)
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            if anim then
                anim:Play()
                anim:AdjustSpeed(1)  -- Set playback speed to 1.5x

                playSoundsSequentially()
                executeAdditionalEffects()  -- Call the new effects function

                -- Wait for 3 seconds before creating particle effects
                wait(1.5)
                createParticleEffect()
            end

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Define the target and replacement animation IDs
local oldAnimID = "16310343179"
local newAnimID = "18846960753"

-- Function to replace animation and play the new animation
local function replaceAndPlayAnimation()
    local humanoid = character:WaitForChild("Humanoid")

    -- Hook into AnimationPlayed event
    humanoid.AnimationPlayed:Connect(function(animationTrack)
        -- Check if the played animation has the old animation ID
        if animationTrack.Animation.AnimationId == "rbxassetid://" .. oldAnimID then
            local animAnim = Instance.new("Animation")
            animAnim.AnimationId = "rbxassetid://" .. newAnimID
            
            local anim = humanoid:LoadAnimation(animAnim)
            anim:Play()

            -- Stop the old animation
            animationTrack:Stop()
        end
    end)
end

-- Initial run to set up animation replacement
replaceAndPlayAnimation()

-- Update the function if the player's character changes
player.CharacterAdded:Connect(function(newCharacter)
    character = newCharacter
    replaceAndPlayAnimation()
end)

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

-- Create the tool
local tool = Instance.new("Tool")
tool.Name = "Death Bringer"
tool.RequiresHandle = false  -- No handle needed for this tool
tool.Parent = player.Backpack

-- Function to teleport the player up and back down
local function teleportUpAndDown()
local currentHeight = humanoidRootPart.Position.Y
local targetHeight = currentHeight + 100  -- teleport 100 studs up
local originalCFrame = humanoidRootPart.CFrame

-- Move player up instantly
humanoidRootPart.CFrame = CFrame.new(humanoidRootPart.Position + Vector3.new(0, 100, 0))

-- Wait for 9.4 seconds
wait(9.4)

-- Move player back to the original position
humanoidRootPart.CFrame = originalCFrame
end

-- Connect the tool's activation event to the teleport function
tool.Activated:Connect(teleportUpAndDown)
