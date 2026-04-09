local CorrectKey = "ASd_123123"
local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local Window = Rayfield:CreateWindow({
   Name = "Saleh Developer",
   KeySystem = true,
   KeySettings = {
      Title = "Enter Key: ASd_123123",
      Key = {CorrectKey}
   }
})
local Main = Window:CreateTab("Main")
Main:CreateInput({
   Name = "Set My Name",
   Callback = function(t)
       local char = game.Players.LocalPlayer.Character
       if char then for _,v in pairs(char:GetDescendants()) do if v:IsA("TextLabel") and v.Visible then v.Text = t end end end
   end,
})
