--[[
    WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk!
]]
-- leave a like pls

_G.HeadSize = 30 -- Reduzido para 30 conforme solicitado
_G.Disabled = true
 
game:GetService('RunService').RenderStepped:Connect(function()
    if _G.Disabled then
        for i, v in next, game:GetService('Players'):GetPlayers() do
            if v.Name ~= game:GetService('Players').LocalPlayer.Name then
                pcall(function()
                    v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize, _G.HeadSize, _G.HeadSize)
                    v.Character.HumanoidRootPart.Transparency = 1 -- Agora totalmente invisível
                    v.Character.HumanoidRootPart.Material = Enum.Material.SmoothPlastic -- Material neutro
                    v.Character.HumanoidRootPart.CanCollide = false
                end)
            end
        end
    end
end)
