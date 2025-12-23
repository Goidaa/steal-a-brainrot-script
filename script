-- Создаем интерфейс программно
local player = game.Players.LocalPlayer
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "TestKeySystem"
screenGui.Parent = player:WaitForChild("PlayerGui")

-- Главное окно
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 300, 0, 150)
frame.Position = UDim2.new(0.5, -150, 0.5, -75)
frame.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
frame.BorderSizePixel = 0
frame.Parent = screenGui

-- Заголовок
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 40)
title.Text = "ВВЕДИТЕ КЛЮЧ"
title.TextColor3 = Color3.new(1, 1, 1)
title.BackgroundTransparency = 1
title.Font = Enum.Font.SourceSansBold
title.TextSize = 20
title.Parent = frame

-- Поле ввода
local textBox = Instance.new("TextBox")
textBox.Size = UDim2.new(0.8, 0, 0, 30)
textBox.Position = UDim2.new(0.1, 0, 0.4, 0)
textBox.PlaceholderText = "Твой ключ здесь..."
textBox.Text = ""
textBox.Parent = frame

-- Кнопка проверки
local button = Instance.new("TextButton")
button.Size = UDim2.new(0.6, 0, 0, 35)
button.Position = UDim2.new(0.2, 0, 0.7, 0)
button.BackgroundColor3 = Color3.fromRGB(0, 170, 0)
button.Text = "Проверить"
button.TextColor3 = Color3.new(1, 1, 1)
button.Parent = frame

-- Логика системы
local CORRECT_KEY = "TEST_2025" -- Твой тестовый ключ

button.MouseButton1Click:Connect(function()
    if textBox.Text == CORRECT_KEY then
        title.Text = "УСПЕШНО!"
        title.TextColor3 = Color3.new(0, 1, 0)
        task.wait(1)
        screenGui:Destroy() -- Удаляем GUI, если ключ верный
        print("Доступ открыт, скрипт сработал.")
    else
        textBox.Text = ""
        textBox.PlaceholderText = "НЕВЕРНЫЙ КЛЮЧ!"
        textBox.PlaceholderColor3 = Color3.new(1, 0, 0)
    end
end)
