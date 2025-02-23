-- Cria uma nova ScreenGui para "CX MODDER"
local screenGuiCX = Instance.new("ScreenGui")
screenGuiCX.Name = "CXScreenGui"
screenGuiCX.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Cria um Frame para o aviso com bordas arredondadas
local frameCX = Instance.new("Frame")
frameCX.Size = UDim2.new(0.3, 0, 0.2, 0)
frameCX.Position = UDim2.new(0.35, 0, 0.4, 0)
frameCX.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
frameCX.BackgroundTransparency = 0.2
frameCX.ClipsDescendants = true
frameCX.Parent = screenGuiCX

-- Adiciona cantos arredondados ao Frame
local cornerCX = Instance.new("UICorner")
cornerCX.CornerRadius = UDim.new(0, 25)
cornerCX.Parent = frameCX

-- Adiciona ttulo ao Frame
local titleCX = Instance.new("TextLabel")
titleCX.Size = UDim2.new(1, 0, 0.3, 0)
titleCX.Position = UDim2.new(0, 0, 0, 0)
titleCX.BackgroundTransparency = 1
titleCX.Text = "CX MODDER"
titleCX.TextColor3 = Color3.fromRGB(255, 255, 255)
titleCX.TextScaled = true
titleCX.Font = Enum.Font.GothamBold
titleCX.Parent = frameCX

-- Adiciona descrio ao Frame
local descriptionCX = Instance.new("TextLabel")
descriptionCX.Size = UDim2.new(1, 0, 0.7, 0)
descriptionCX.Position = UDim2.new(0, 0, 0.3, 0)
descriptionCX.BackgroundTransparency = 1
descriptionCX.Text = "Este menu foi feito pelo CXMODDER"
descriptionCX.TextColor3 = Color3.fromRGB(255, 255, 255)
descriptionCX.TextScaled = true
descriptionCX.Font = Enum.Font.Gotham
descriptionCX.Parent = frameCX

-- Torna o ScreenGui "CX MODDER" invisvel aps 5 segundos e abre o prximo ScreenGui
delay(5, function()
    screenGuiCX.Enabled = false

    -- Cria uma nova ScreenGui para "SEMI-UNIVERSAL AIMBOT"
    local screenGui = Instance.new("ScreenGui")
    screenGui.Name = "MainScreenGui"
    screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

    -- Cria um Frame para o aviso com bordas arredondadas
    local frame = Instance.new("Frame")
    frame.Size = UDim2.new(0, 0, 0, 0)  -- Comea pequeno
    frame.Position = UDim2.new(0.35, 0, 0.4, 0)
    frame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
    frame.BackgroundTransparency = 0.2
    frame.ClipsDescendants = true
    frame.Parent = screenGui

    -- Adiciona cantos arredondados ao Frame
    local corner = Instance.new("UICorner")
    corner.CornerRadius = UDim.new(0, 25)
    corner.Parent = frame

    -- Adiciona ttulo ao Frame
    local title = Instance.new("TextLabel")
    title.Size = UDim2.new(1, 0, 0.3, 0)
    title.Position = UDim2.new(0, 0, 0, 0)
    title.BackgroundTransparency = 1
    title.Text = "SEMI-UNIVERSAL AIMBOT"
    title.TextColor3 = Color3.fromRGB(255, 255, 255)
    title.TextScaled = true
    title.Font = Enum.Font.GothamBold
    title.Parent = frame

    -- Adiciona boto grande "EXECUTE" ao Frame
    local executeButton = Instance.new("TextButton")
    executeButton.Size = UDim2.new(0.8, 0, 0.5, 0)
    executeButton.Position = UDim2.new(0.1, 0, 0.4, 0)
    executeButton.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
    executeButton.Text = "EXECUTE"
    executeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    executeButton.TextScaled = true
    executeButton.Font = Enum.Font.GothamBold
    executeButton.Parent = frame
    executeButton.AutoButtonColor = false  -- Desativa a mudana de cor automtica do boto

    -- Adiciona cantos arredondados ao boto
    local buttonCorner = Instance.new("UICorner")
    buttonCorner.CornerRadius = UDim.new(0, 15)
    buttonCorner.Parent = executeButton

    -- Funo para mostrar o dilogo
    local function showDialog(title, description, duration)
        game.StarterGui:SetCore("SendNotification", {
            Title = title;
            Text = description;
            Duration = duration;
        })
    end

    -- Animao de entrada
    local TweenService = game:GetService("TweenService")
    local tweenInfo = TweenInfo.new(3, Enum.EasingStyle.Quint, Enum.EasingDirection.Out)
    local tween = TweenService:Create(frame, tweenInfo, {Size = UDim2.new(0.3, 0, 0.2, 0)})
    tween:Play()

    -- Funo para executar o cdigo ao clicar no boto
    executeButton.MouseButton1Click:Connect(function()
        if executeButton.Text == "EXECUTED" or executeButton.Text ~= "EXECUTE" then
            return -- Evita a execuo dupla do script
        end
        
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Lk28s/Aimfov1/main/Wall%2BTeamCheck"))();
        executeButton.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
        executeButton.Text = "EXECUTED"
        executeButton.AutoButtonColor = false  -- Desativa a mudana de cor automtica do boto
        showDialog("Ateno", "O cdigo foi executado com sucesso!", 10)

        -- Inicia a contagem regressiva aps 3 segundos
        wait(3)
        executeButton.BackgroundColor3 = Color3.fromRGB(255, 255, 0)
        for i = 10, 1, -1 do
            if i <= 4 then
                executeButton.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
            end
            executeButton.Text = tostring(i)
            wait(1)
        end

        -- Mostra o dilogo antes de destruir o ScreenGui
        showDialog("AVISO", "O menu foi destrudo", 10)

        -- Destroi o ScreenGui aps a contagem regressiva
        screenGui:Destroy()
    end)
end)
