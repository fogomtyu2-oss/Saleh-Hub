local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "Saleh Hub | صالح ديف",
   LoadingTitle = "جاري التشغيل...",
   LoadingSubtitle = "بواسطة صالح",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = "SalehHub",
      FileName = "Config"
   },
   KeySystem = true,
   KeySettings = {
      Title = "نظام المفتاح",
      Subtitle = "المفتاح هو: ASd_123123",
      Note = "اكتب المفتاح للدخول",
      FileName = "Key",
      SaveKey = true,
      GrabKeyFromSite = false,
      Key = {"ASd_123123"}
   }
})

local Tab = Window:CreateTab("الرئيسية", 4483362458)

Tab:CreateButton({
   Name = "تغيير اسمي (تجربة)",
   Callback = function()
       local char = game.Players.LocalPlayer.Character
       if char then 
           for _,v in pairs(char:GetDescendants()) do 
               if v:IsA("TextLabel") and v.Visible then v.Text = "SALEH DEV" end 
           end 
       end
   end,
})

Rayfield:Notify({
   Title = "تم التشغيل!",
   Content = "استمتع بالسكربت يا صالح",
   Duration = 5,
   Image = 4483362458,
})
