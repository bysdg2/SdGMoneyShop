
-- ==== Manu ====
    while true do wait() -- เช็คว่าคนเข้าเกมค่อยรัน script
        if game.Players.LocalPlayer then
            break
        end
    end
    wait(_G.TimeDelay)

    local Flux = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/fluxlib.txt")() -- UI
    local win = Flux:Window("SdG Money", "Team SdG", Color3.fromRGB(250, 138, 0), Enum.KeyCode.RightControl)
    local tab = win:Tab("FullAuto", "http://www.roblox.com/asset/?id=6023426915")
    local mastery = win:Tab("Mastery Fruit or Gun", "http://www.roblox.com/asset/?id=6023426915")
    local dungeon = win:Tab("Dungeon", "http://www.roblox.com/asset/?id=6023426915")
    local misc = win:Tab("Misc", "http://www.roblox.com/asset/?id=6023426915")
    local vs = win:Tab("SdGMoneyShop", "http://www.roblox.com/asset/?id=6023426915")
    local vs1 = win:Tab("Version 2.0a", "http://www.roblox.com/asset/?id=6023426915")

    OldWorld = false
    newworld = false
    local MyLevel = game.Players.localPlayer.Data.Level.Value
    local placeId = game.PlaceId
    if placeId == 2753915549 then
        OldWorld = true
    elseif placeId == 4442272183 then
        newworld = true
    end
    SelectDevil = ""

    local LocalPlayer = game:GetService("Players").LocalPlayer
    local VirtualUser = game:GetService('VirtualUser')
    local N=game:GetService("VirtualInputManager")
    local pirateSide, marineSide = game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton, game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton

    wait(1)
    N:SendKeyEvent(true,"RightControl",false,game)
    wait(0.1)
    N:SendKeyEvent(false,"RightControl",false,game)
    wait(1)
    for i,v in pairs(getconnections(pirateSide.MouseButton1Click)) do
        v:Function()
    end

    local toweapon = {
        [1] = "Combat",
        [2] = "Death Step",
        [3] = "Black Leg",
        [4] = "Electro",
        [5] = "Fishman Karate",
        [6] = "Dragon Claw",
        [7] = "Superhuman"
    }
    -- เช็คมอส และ เควส
    function CheckQuest()
        local MyLevel = game.Players.localPlayer.Data.Level.Value
        if OldWorld then
            if MyLevel == 1 or MyLevel <= 9 then -- Bandit
                Ms = "Bandit [Lv. 5]"
                NameMon = "Bandit"
                NaemQuest = "BanditQuest1"
                LevelQuest = 1
                CFrameQuest = CFrame.new(1061.66699, 16.5166187, 1544.52905, -0.942978859, -3.33851502e-09, 0.332852632, 7.04340497e-09, 1, 2.99841325e-08, -0.332852632, 3.06188177e-08, -0.942978859)
                CFrameMon = CFrame.new(1199.31287, 52.2717781, 1536.91516, -0.929782331, 6.60215846e-08, -0.368109822, 3.9077392e-08, 1, 8.06501603e-08, 0.368109822, 6.06023249e-08, -0.929782331)
            elseif MyLevel == 10 or MyLevel <= 14 then -- Monkey
                Ms = "Monkey [Lv. 14]"
                NameMon = "Monkey"
                NaemQuest = "JungleQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
                CFrameMon = CFrame.new(-1567.92639, 60.4013481, 6.84663391, -0.866364598, -0.000311239448, -0.499412209, -0.000355866447, 0.99999994, -5.86570968e-06, 0.499412149, 0.000172642176, -0.866364717)
            elseif MyLevel == 15 or MyLevel <= 29 then -- Gorilla
                Ms = "Gorilla [Lv. 20]"
                NameMon = "Gorilla"
                NaemQuest = "JungleQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
                CFrameMon = CFrame.new(-1223.52808, 6.27936459, -502.292664, 0.310949147, -5.66602516e-08, 0.950426519, -3.37275488e-08, 1, 7.06501808e-08, -0.950426519, -5.40241736e-08, 0.310949147)
            elseif MyLevel == 30 or MyLevel <= 39 then -- Pirate
                Ms = "Pirate [Lv. 35]"
                NameMon = "Pirate"
                NaemQuest = "BuggyQuest1"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
                CFrameMon = CFrame.new(-1219.32324, 4.75205183, 3915.63452, -0.966492832, -6.91238853e-08, 0.25669381, -5.21195496e-08, 1, 7.3047012e-08, -0.25669381, 5.72206496e-08, -0.966492832)
            elseif MyLevel == 40 or MyLevel <= 59 then -- ÚBrute
                Ms = "Brute [Lv. 45]"
                NameMon = "Brute"
                NaemQuest = "BuggyQuest1"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
                CFrameMon = CFrame.new(-1146.49646, 96.0936813, 4312.1333, -0.978175163, -1.53222057e-08, 0.207781896, -3.33316912e-08, 1, -8.31738873e-08, -0.207781896, -8.82843523e-08, -0.978175163)
            elseif MyLevel == 60 or MyLevel <= 74 then -- Desert Bandit
                Ms = "Desert Bandit [Lv. 60]"
                NameMon = "Desert Bandit"
                NaemQuest = "DesertQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
                CFrameMon = CFrame.new(932.788818, 6.4503746, 4488.24609, -0.998625934, 3.08948351e-08, 0.0524050146, 2.79967303e-08, 1, -5.60361286e-08, -0.0524050146, -5.44919629e-08, -0.998625934)
            elseif MyLevel == 75 or MyLevel <= 89 then -- Desert Officre
                Ms = "Desert Officer [Lv. 70]"
                NameMon = "Desert Officer"
                NaemQuest = "DesertQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
                CFrameMon = CFrame.new(1580.03198, 4.61375761, 4366.86426, 0.135744005, -6.44280718e-08, -0.990743816, 4.35738308e-08, 1, -5.90598574e-08, 0.990743816, -3.51534837e-08, 0.135744005)
            elseif MyLevel == 90 or MyLevel <= 99 then -- Snow Bandits
                Ms = "Snow Bandit [Lv. 90]"
                NameMon = "Snow Bandit"
                NaemQuest = "SnowQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
                CFrameMon = CFrame.new(1370.24316, 102.403511, -1411.52905, 0.980274439, -1.12995728e-08, 0.197641045, -9.57343449e-09, 1, 1.04655214e-07, -0.197641045, -1.04482936e-07, 0.980274439)
            elseif MyLevel == 100 or MyLevel <= 119 then -- Snowman
                Ms = "Snowman [Lv. 100]"
                NameMon = "Snowman" 
                NaemQuest = "SnowQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
                CFrameMon = CFrame.new(1370.24316, 102.403511, -1411.52905, 0.980274439, -1.12995728e-08, 0.197641045, -9.57343449e-09, 1, 1.04655214e-07, -0.197641045, -1.04482936e-07, 0.980274439)
            elseif MyLevel == 120 or MyLevel <= 149 then -- Chief Petty Officer
                Ms = "Chief Petty Officer [Lv. 120]"
                NameMon = "Chief Petty Officer"
                NaemQuest = "MarineQuest2"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-5035.0835, 28.6520386, 4325.29443, 0.0243340395, -7.08064647e-08, 0.999703884, -6.36926814e-08, 1, 7.23777944e-08, -0.999703884, -6.54350671e-08, 0.0243340395)
                CFrameMon = CFrame.new(-4882.8623, 22.6520386, 4255.53516, 0.273695946, -5.40380647e-08, -0.96181643, 4.37720793e-08, 1, -4.37274998e-08, 0.96181643, -3.01326679e-08, 0.273695946)
            elseif MyLevel == 150 or MyLevel <= 174 then -- Sky Bandit
                Ms = "Sky Bandit [Lv. 150]"
                NameMon = "Sky Bandit"
                NaemQuest = "SkyQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)
                CFrameMon = CFrame.new(-4970.74219, 294.544342, -2890.11353, -0.994874597, -8.61311236e-08, -0.101116329, -9.10836206e-08, 1, 4.43614923e-08, 0.101116329, 5.33441664e-08, -0.994874597)
            elseif MyLevel == 175 or MyLevel <= 224 then -- Dark Master
                Ms = "Dark Master [Lv. 175]"
                NameMon = "Dark Master"
                NaemQuest = "SkyQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)
                CFrameMon = CFrame.new(-5220.58594, 430.693298, -2278.17456, -0.925375521, 1.12086873e-08, 0.379051805, -1.05115507e-08, 1, -5.52320891e-08, -0.379051805, -5.50948407e-08, -0.925375521)
            elseif MyLevel == 225 or MyLevel <= 274 then -- Toga Warrior
                Ms = "Toga Warrior [Lv. 225]"
                NameMon = "Toga Warrior"
                NaemQuest = "ColosseumQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)
                CFrameMon = CFrame.new(-1779.97583, 44.6077499, -2736.35474, 0.984437346, 4.10396339e-08, 0.175734788, -3.62286876e-08, 1, -3.05844168e-08, -0.175734788, 2.3741821e-08, 0.984437346)
            elseif MyLevel == 275 or MyLevel <= 299 then -- Gladiato
                Ms = "Gladiator [Lv. 275]"
                NameMon = "Gladiator"
                NaemQuest = "ColosseumQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)
                CFrameMon = CFrame.new(-1274.75903, 58.1895943, -3188.16309, 0.464524001, 6.21005611e-08, 0.885560572, -4.80449414e-09, 1, -6.76054768e-08, -0.885560572, 2.71497012e-08, 0.464524001)
            elseif MyLevel == 300 or MyLevel <= 329 then -- Military Soldier
                Ms = "Military Soldier [Lv. 300]"
                NameMon = "Military Soldier"
                NaemQuest = "MagmaQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
                CFrameMon = CFrame.new(-5363.01123, 41.5056877, 8548.47266, -0.578253984, -3.29503091e-10, 0.815856814, 9.11209668e-08, 1, 6.498761e-08, -0.815856814, 1.11920997e-07, -0.578253984)
            elseif MyLevel == 300 or MyLevel <= 374 then -- Military Spy
                Ms = "Military Spy [Lv. 330]"
                NameMon = "Military Spy"
                NaemQuest = "MagmaQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
                CFrameMon = CFrame.new(-5787.99023, 120.864456, 8762.25293, -0.188358366, -1.84706277e-08, 0.982100308, -1.23782129e-07, 1, -4.93306951e-09, -0.982100308, -1.22495649e-07, -0.188358366)
            elseif MyLevel == 375 or MyLevel <= 399 then -- Fishman Warrior
                Ms = "Fishman Warrior [Lv. 375]"
                NameMon = "Fishman Warrior"
                NaemQuest = "FishmanQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
                CFrameMon = CFrame.new(60946.6094, 48.6735229, 1525.91687, -0.0817126185, 8.90751153e-08, 0.996655822, 2.00889794e-08, 1, -8.77269599e-08, -0.996655822, 1.28533992e-08, -0.0817126185)
            elseif MyLevel == 400 or MyLevel <= 449 then -- Fishman Commando
                Ms = "Fishman Commando [Lv. 400]"
                NameMon = "Fishman Commando"
                NaemQuest = "FishmanQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
                CFrameMon = CFrame.new(61885.5039, 18.4828243, 1504.17896, 0.577502489, 0, -0.816389024, -0, 1.00000012, -0, 0.816389024, 0, 0.577502489)
            elseif MyLevel == 450 or MyLevel <= 474 then -- God's Guards
                Ms = "God's Guard [Lv. 450]"
                NameMon = "God's Guard"
                NaemQuest = "SkyExp1Quest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-4721.71436, 845.277161, -1954.20105, -0.999277651, -5.56969759e-09, 0.0380011722, -4.14751478e-09, 1, 3.75035256e-08, -0.0380011722, 3.73188307e-08, -0.999277651)
                CFrameMon = CFrame.new(-4716.95703, 853.089722, -1933.92542, -0.93441087, -6.77488776e-09, -0.356197298, 1.12145182e-08, 1, -4.84390199e-08, 0.356197298, -4.92565206e-08, -0.93441087)
            elseif MyLevel == 475 or MyLevel <= 524 then -- Shandas
                Ms = "Shanda [Lv. 475]"
                NameMon = "Shanda"
                NaemQuest = "SkyExp1Quest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-7863.63672, 5545.49316, -379.826324, 0.362120807, -1.98046344e-08, -0.93213129, 4.05822291e-08, 1, -5.48095125e-09, 0.93213129, -3.58431969e-08, 0.362120807)
                CFrameMon = CFrame.new(-7685.12354, 5601.05127, -443.171509, 0.150056243, 1.79768236e-08, -0.988677442, 6.67798661e-09, 1, 1.91962481e-08, 0.988677442, -9.48289181e-09, 0.150056243)
            elseif MyLevel == 525 or MyLevel <= 549 then -- Royal Squad
                Ms = "Royal Squad [Lv. 525]"
                NameMon = "Royal Squad"
                NaemQuest = "SkyExp2Quest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
                CFrameMon = CFrame.new(-7685.02051, 5606.87842, -1442.729, 0.561947823, 7.69527464e-09, -0.827172697, -4.24974544e-09, 1, 6.41599973e-09, 0.827172697, -9.01838604e-11, 0.561947823)
            elseif MyLevel == 550 or MyLevel <= 624 then -- Royal Soldier
                Ms = "Royal Soldier [Lv. 550]"
                NameMon = "Royal Soldier"
                NaemQuest = "SkyExp2Quest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
                CFrameMon = CFrame.new(-7864.44775, 5661.94092, -1708.22351, 0.998389959, 2.28686137e-09, -0.0567218624, 1.99431383e-09, 1, 7.54200258e-08, 0.0567218624, -7.54117195e-08, 0.998389959)
            elseif MyLevel == 625 or MyLevel <= 649 then -- Galley Pirate
                Ms = "Galley Pirate [Lv. 625]"
                NameMon = "Galley Pirate"
                NaemQuest = "FountainQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
                CFrameMon = CFrame.new(5595.06982, 41.5013695, 3961.47095, -0.992138803, -2.11610267e-08, -0.125142589, -1.34249509e-08, 1, -6.26613996e-08, 0.125142589, -6.04887518e-08, -0.992138803)
            elseif MyLevel >= 650 then -- Galley Captain
                Ms = "Galley Captain [Lv. 650]"
                NameMon = "Galley Captain"
                NaemQuest = "FountainQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
                CFrameMon = CFrame.new(5658.5752, 38.5361786, 4928.93506, -0.996873081, 2.12391046e-06, -0.0790185928, 2.16989656e-06, 1, -4.96097414e-07, 0.0790185928, -6.66008248e-07, -0.996873081)
            end
        end
        if newworld then
            if MyLevel == 700 or MyLevel <= 724 then -- Raider [Lv. 700]
                Ms = "Raider [Lv. 700]"
                NameMon = "Raider" 
                NaemQuest = "Area1Quest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601, -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
                CFrameMon = CFrame.new(-737.026123, 39.1748352, 2392.57959, 0.272128761, 0, -0.962260842, -0, 1, -0, 0.962260842, 0, 0.272128761)
            elseif MyLevel == 725 or MyLevel <= 774 then -- Mercenary [Lv. 725]
                Ms = "Mercenary [Lv. 725]"
                NameMon = "Mercenary" 
                NaemQuest = "Area1Quest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601, -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
                CFrameMon = CFrame.new(-973.731995, 95.8733215, 1836.46936, 0.999135971, 2.02326991e-08, -0.0415605344, -1.90767793e-08, 1, 2.82094952e-08, 0.0415605344, -2.73922804e-08, 0.999135971)
            elseif MyLevel == 775 or MyLevel <= 799 then -- Swan Pirate [Lv. 775]
                Ms = "Swan Pirate [Lv. 775]"
                NameMon = "Swan Pirate" 
                NaemQuest = "Area2Quest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
                CFrameMon = CFrame.new(970.369446, 142.653198, 1217.3667, 0.162079468, -4.85452638e-08, -0.986777723, 1.03357589e-08, 1, -4.74980872e-08, 0.986777723, -2.50063148e-09, 0.162079468)
            elseif MyLevel == 800 or MyLevel <= 874 then -- Factory Staff [Lv. 800]
                Ms = "Factory Staff [Lv. 800]"
                NameMon = "Factory Staff" 
                NaemQuest = "Area2Quest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
                CFrameMon = CFrame.new(296.786499, 72.9948196, -57.1298141, -0.876037002, -5.32364979e-08, 0.482243896, -3.87658332e-08, 1, 3.99718729e-08, -0.482243896, 1.63222538e-08, -0.876037002)
            elseif MyLevel == 875 or MyLevel <= 899 then -- Marine Lieutenant [Lv. 875]
                Ms = "Marine Lieutenant [Lv. 875]"
                NameMon = "Marine Lieutenant" 
                NaemQuest = "MarineQuest3"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301, 5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)
                CFrameMon = CFrame.new(-2913.26367, 73.0011826, -2971.64282, 0.910507619, 0, 0.413492233, 0, 1.00000012, 0, -0.413492233, 0, 0.910507619)
            elseif MyLevel == 900 or MyLevel <= 949 then -- Marine Captain [Lv. 900]
                Ms = "Marine Captain [Lv. 900]"
                NameMon = "Marine Captain" 
                NaemQuest = "MarineQuest3"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301, 5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)
                CFrameMon = CFrame.new(-1868.67688, 73.0011826, -3321.66333, -0.971402287, 1.06502087e-08, 0.237439692, 3.68856199e-08, 1, 1.06050372e-07, -0.237439692, 1.11775684e-07, -0.971402287)
            elseif MyLevel == 950 or MyLevel <= 974 then -- Zombie [Lv. 950]
                Ms = "Zombie [Lv. 950]"
                NameMon = "Zombie" 
                NaemQuest = "ZombieQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742, 4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)
                CFrameMon = CFrame.new(-5634.83838, 126.067039, -697.665039, -0.992770672, 6.77618939e-09, 0.120025545, 1.65461245e-08, 1, 8.04023372e-08, -0.120025545, 8.18070234e-08, -0.992770672)
            elseif MyLevel == 975 or MyLevel <= 999 then -- Vampire [Lv. 975]
                Ms = "Vampire [Lv. 975]"
                NameMon = "Vampire" 
                NaemQuest = "ZombieQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742, 4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)
                CFrameMon = CFrame.new(-6030.32031, 6.4377408, -1313.5564, -0.856965423, 3.9138893e-08, -0.515373945, -1.12178942e-08, 1, 9.45958547e-08, 0.515373945, 8.68467822e-08, -0.856965423)
            elseif MyLevel == 1000 or MyLevel <= 1049 then -- Snow Trooper [Lv. 1000] **
                Ms = "Snow Trooper [Lv. 1000]"
                NameMon = "Snow Trooper" 
                NaemQuest = "SnowMountainQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(604.964966, 401.457062, -5371.69287, 0.353063971, 1.89520435e-08, -0.935599446, -5.81846002e-08, 1, -1.70033754e-09, 0.935599446, 5.50377841e-08, 0.353063971)
                CFrameMon = CFrame.new(535.893433, 401.457062, -5329.6958, -0.999524176, 0, 0.0308452044, 0, 1, -0, -0.0308452044, 0, -0.999524176)
            elseif MyLevel == 1050 or MyLevel <= 1099 then -- Winter Warrior [Lv. 1050]
                Ms = "Winter Warrior [Lv. 1050]"
                NameMon = "Winter Warrior" 
                NaemQuest = "SnowMountainQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(604.964966, 401.457062, -5371.69287, 0.353063971, 1.89520435e-08, -0.935599446, -5.81846002e-08, 1, -1.70033754e-09, 0.935599446, 5.50377841e-08, 0.353063971)
                CFrameMon = CFrame.new(1223.7417, 454.575226, -5170.02148, 0.473996818, 2.56845354e-08, 0.880526543, -5.62456428e-08, 1, 1.10811016e-09, -0.880526543, -5.00510211e-08, 0.473996818)
            elseif MyLevel == 1100 or MyLevel <= 1124 then -- Lab Subordinate [Lv. 1100]
                Ms = "Lab Subordinate [Lv. 1100]"
                NameMon = "Lab Subordinate" 
                NaemQuest = "IceSideQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528, 1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)
                CFrameMon = CFrame.new(-5769.2041, 37.9288292, -4468.38721, -0.569419742, -2.49055017e-08, 0.822046936, -6.96206541e-08, 1, -1.79282633e-08, -0.822046936, -6.74401548e-08, -0.569419742)
            elseif MyLevel == 1125 or MyLevel <= 1174 then -- Horned Warrior [Lv. 1125]
                Ms = "Horned Warrior [Lv. 1125]"
                NameMon = "Horned Warrior" 
                NaemQuest = "IceSideQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528, 1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)
                CFrameMon = CFrame.new(-6400.85889, 24.7645149, -5818.63574, -0.964845479, 8.65926566e-08, -0.262817472, 3.98261392e-07, 1, -1.13260398e-06, 0.262817472, -1.19745812e-06, -0.964845479)
            elseif MyLevel == 1175 or MyLevel <= 1199 then -- Magma Ninja [Lv. 1175]
                Ms = "Magma Ninja [Lv. 1175]"
                NameMon = "Magma Ninja" 
                NaemQuest = "FireSideQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-5431.09473, 15.9868021, -5296.53223, 0.831796765, 1.15322464e-07, -0.555080295, -1.10814341e-07, 1, 4.17010995e-08, 0.555080295, 2.68240168e-08, 0.831796765)
                CFrameMon = CFrame.new(-5496.65576, 58.6890411, -5929.76855, -0.885073781, 0, -0.465450764, 0, 1.00000012, -0, 0.465450764, 0, -0.885073781)
            elseif MyLevel == 1200 or MyLevel <= 1249 then -- Lava Pirate [Lv. 1200]
                Ms = "Lava Pirate [Lv. 1200]"
                NameMon = "Lava Pirate" 
                NaemQuest = "FireSideQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-5431.09473, 15.9868021, -5296.53223, 0.831796765, 1.15322464e-07, -0.555080295, -1.10814341e-07, 1, 4.17010995e-08, 0.555080295, 2.68240168e-08, 0.831796765)
                CFrameMon = CFrame.new(-5169.71729, 34.1234779, -4669.73633, -0.196780294, 0, 0.98044765, 0, 1.00000012, -0, -0.98044765, 0, -0.196780294)
            elseif MyLevel == 1250 or MyLevel <= 1274 then -- Ship Deckhand [Lv. 1250]
                Ms = "Ship Deckhand [Lv. 1250]"
                NameMon = "Ship Deckhand" 
                NaemQuest = "ShipQuest1"
                LevelQuest = 1
                CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)
                CFrameMon = CFrame.new(1163.80872, 138.288452, 33058.4258, -0.998580813, 5.49076979e-08, -0.0532564968, 5.57436763e-08, 1, -1.42118655e-08, 0.0532564968, -1.71604082e-08, -0.998580813)
            elseif MyLevel == 1275 or MyLevel <= 1299 then -- Ship Engineer [Lv. 1275]
                Ms = "Ship Engineer [Lv. 1275]"
                NameMon = "Ship Engineer" 
                NaemQuest = "ShipQuest1"
                LevelQuest = 2
                CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)
                CFrameMon = CFrame.new(916.666504, 44.0920448, 32917.207, -0.99746871, -4.85034697e-08, -0.0711069331, -4.8925461e-08, 1, 4.19294288e-09, 0.0711069331, 7.66126895e-09, -0.99746871)
            elseif MyLevel == 1300 or MyLevel <= 1324 then -- Ship Steward [Lv. 1300]
                Ms = "Ship Steward [Lv. 1300]"
                NameMon = "Ship Steward" 
                NaemQuest = "ShipQuest2"
                LevelQuest = 1
                CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)
                CFrameMon = CFrame.new(918.743286, 129.591064, 33443.4609, -0.999792814, -1.7070947e-07, -0.020350717, -1.72559169e-07, 1, 8.91351277e-08, 0.020350717, 9.2628369e-08, -0.999792814)
            elseif MyLevel == 1325 or MyLevel <= 1349 then -- Ship Officer [Lv. 1325]
                Ms = "Ship Officer [Lv. 1325]"
                NameMon = "Ship Officer" 
                NaemQuest = "ShipQuest2"
                LevelQuest = 2
                CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)
                CFrameMon = CFrame.new(786.051941, 181.474106, 33303.2969, 0.999285698, -5.32193063e-08, 0.0377905183, 5.68968588e-08, 1, -9.62386864e-08, -0.0377905183, 9.83201005e-08, 0.999285698)
            elseif MyLevel == 1350 or MyLevel <= 1374 then -- Arctic Warrior [Lv. 1350]
                Ms = "Arctic Warrior [Lv. 1350]"
                NameMon = "Arctic Warrior" 
                NaemQuest = "FrostQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226, -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)
                CFrameMon = CFrame.new(5995.07471, 57.3188477, -6183.47314, 0.702747107, -1.53454167e-07, -0.711440146, -1.08168464e-07, 1, -3.22542007e-07, 0.711440146, 3.03620908e-07, 0.702747107)
            elseif MyLevel == 1375 or MyLevel <= 1425 then -- Snow Lurker [Lv. 1375]
                Ms = "Snow Lurker [Lv. 1375]"
                NameMon = "Snow Lurker" 
                NaemQuest = "FrostQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226, -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)
                CFrameMon = CFrame.new(5518.00684, 60.5559731, -6828.80518, -0.650781393, -3.64292951e-08, 0.759265184, -4.07668654e-09, 1, 4.44854642e-08, -0.759265184, 2.58550248e-08, -0.650781393)
            elseif MyLevel == 1425 or MyLevel <= 1450 then
                Ms = "Sea Soldier [Lv. 1425]"
                NameMon = "Sea Soldier" 
                NaemQuest = "ForgottenQuest"
                LevelQuest = 1
                CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
                CFrameMon = CFrame.new(-3353.53613, 26.9538937, -9769.85938, 0.463716149, 2.65137445e-09, 0.885983825, -1.27188049e-09, 1, -2.32688557e-09, -0.885983825, -4.78510738e-11, 0.463716149)
            elseif MyLevel >= 1450 then
                Ms = "Water Fighter [Lv. 1450]"
                NameMon = "Water Fighter"
                NaemQuest = "ForgottenQuest"
                LevelQuest = 2
                CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
                CFrameMon = CFrame.new(-3496.54175, 238.84613, -10511.5869, 0.453124046, -0.00694153132, 0.891420722, 0.00689816847, 0.999967039, 0.00428033061, -0.891421199, 0.00420964789, 0.453157187)

            end
        end
    end

    tab:Toggle("FullAutoFarm LevelMax + Mastery + Raid + Hop", "", _G.ModeFull, function(vu)
        if vu then
            local CheckLevel = game.Players.LocalPlayer.Data.Level.Value
            if CheckLevel == 1525 then 
                FullLevelMaxMasteryRaid = vu
            else
                AFM = vu
                AutoNewWord = vu
                autosuperhuman = vu
            end
        else
            FullLevelMaxMasteryRaid = vu
            AFM = vu
            AutoNewWord = vu
            autosuperhuman = vu
        end
    end)
    tab:Toggle("FullAutoFarm LevelMax", "", _G.ModeAutoFarmLock1525, function(vu)
        if vu then
            AFM = vu
            autosuperhuman = vu
            AutoNewWord = vu
            FullLevelMax = vu
        else
            AFM = vu
            autosuperhuman = vu
            AutoNewWord = vu
            FullLevelMax = vu
        end
    end)
    tab:Toggle("FullAutoFarm Level 700", "", _G.ModeAutoFarmLock700, function(vu)
        if vu then
            AFM = vu
            autosuperhuman = vu
            AutoNewWord = vu
            FullLevel700 = vu
        else
            AFM = vu
            autosuperhuman = vu
            AutoNewWord = vu
            FullLevel700 = vu
        end
    end)
    mastery:Toggle("Auto Mastery Devil Fruit", "", false, function(vu)
        Mastery = vu
    end)
    mastery:Toggle("Auto Fram Gun Mastery","",false,function(v)
        if WeaponMastery == "" and v then
            VLib:Notification("Select Weapon First")
        else 
            CheckQuest()
            local args = {
                    [1] = "AbandonQuest"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            GunMastery = v
            Ms = ""
        end	
        while GunMastery do wait()
        AutoGunMastery()
        end
    end)
    Wapon = {}
    pcall(function()
        for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
            if v.ToolTip == "Sword" then
            table.insert(Wapon ,v.Name)
            end
        end
        for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
            if v.ToolTip == "Sword" then
            table.insert(Wapon ,v.Name)
            end
        end
    end)
    local AMS = mastery:Dropdown("Select Weapon",Wapon,function(Value)
        WeaponMastery = Value
    end)
    mastery:Button("Refresh Weapon","",function()
        AMS:Clear()
        pcall(function()
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
                if v.ToolTip == "Sword" then
                AMS:Add(v.Name)
            end
            end
            for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
                if v.ToolTip == "Sword" then
                AMS:Add(v.Name)
                end
            end
        end)
    end)
    dungeon:Toggle("AutoRaid", "", false, function(vu)
        if vu then 
            raid = vu
        end
    end)
    dungeon:Toggle("Room 2", "", false, function(vu)
        if vu then
            room1 = vu
        else
            room1 = vu
        end
    end)
    dungeon:Toggle("Room 3", "", false, function(vu)
        if vu then
            room2 = vu
        else
            room2 = vu
        end
    end)
    dungeon:Toggle("Room 4", "", false, function(vu)
        if vu then
            room3 = vu
        else
            room3 = vu
        end
    end)
    misc:Toggle("Open Fog", "",false, function(vu)
        while true do
            wait(1)
            if vu then 
                game.Lighting.FogEnd = 150
            else
                game.Lighting.FogEnd = 1000000
            end
        end
    end)
    misc:Toggle("ClickTP R + Click", "",false, function(vu)
        local player = game:GetService("Players").LocalPlayer
        local char = player.Character
        local mouse = player:GetMouse()
        local uis = game:GetService("UserInputService")

        local shifthold  = vu

        mouse.Button1Down:Connect(function()
            if shifthold then
                char:MoveTo(mouse.Hit.p)
            end
        end)

        uis.InputBegan:Connect(function(input, process)
            if input.KeyCode == Enum.KeyCode.R then
                shifthold = true
            end
        end)

        uis.InputEnded:Connect(function(input, process)
            if input.KeyCode == Enum.KeyCode.R then
                shifthold = false
            end
        end)
    end)
    misc:Button("Server Hop", "", function()
        Teleport()
    end)
    misc:Button("Inventory", "", function()
        game:GetService("Players").LocalPlayer.PlayerGui.Main.Inventory.Visible = true
    end)
    misc:Button("FruitShop", "", function()
        game:GetService("Players").LocalPlayer.PlayerGui.Main.FruitShop.Visible = true
    end)
    misc:Button("AwakeningToggler", "", function()
        game:GetService("Players").LocalPlayer.PlayerGui.Main.AwakeningToggler.Visible = true
    end)
-- ==== Manu ====
-- =====  Weapon  =====
    function EquipWeapon(ToolSe)
        if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
            local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
            wait(.4)
            game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
        end
    end
-- =====  Weapon  =====

-- ==== Full AutoFarm LevelMax + Mastery + Raid ====
    spawn(function()
        while wait() do 
            wait(2)
            if FullLevelMaxMasteryRaid then
                local CheckLevel = game.Players.LocalPlayer.Data.Level.Value
                local CheckFruits = game:GetService("Players").localPlayer.Data.DevilFruit.Value
                for i,v in pairs(game:GetService("Players").localPlayer.Backpack:GetChildren()) do
                    if v.Name == "Flame-Flame" then
                        if CheckLevel == 1525 and v.Level.Value >= 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 100 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Ice-Ice" then
                        if CheckLevel == 1525 and v.Level.Value >= 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 100 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Dark-Dark" then
                        if CheckLevel == 1525 and v.Level.Value >= 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 110 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Light-Light" then
                        if CheckLevel == 1525 and v.Level.Value >= 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 110 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Quake-Quake" then
                        if CheckLevel == 1525 and v.Level.Value >= 150 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 150 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 150 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "String-String" then
                        if CheckLevel == 1525 and v.Level.Value >= 225 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 225 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 225 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Rumble-Rumble" then
                        if CheckLevel == 1525 and v.Level.Value >= 250 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 250 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 250 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    end
                end
                for i,v in pairs(game:GetService("Players").localPlayer.Character:GetChildren()) do
                    if v.Name == "Flame-Flame" then
                        if CheckLevel == 1525 and v.Level.Value >= 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 100 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Ice-Ice" then
                        if CheckLevel == 1525 and v.Level.Value >= 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 100 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 100 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Dark-Dark" then
                        if CheckLevel == 1525 and v.Level.Value >= 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 110 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Light-Light" then
                        if CheckLevel == 1525 and v.Level.Value >= 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 110 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 110 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Quake-Quake" then
                        if CheckLevel == 1525 and v.Level.Value >= 150 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 150 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 150 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "String-String" then
                        if CheckLevel == 1525 and v.Level.Value >= 225 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 225 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 225 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    elseif v.Name == "Rumble-Rumble" then
                        if CheckLevel == 1525 and v.Level.Value >= 250 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = true
                        elseif CheckLevel == 1525 and v.Level.Value < 250 and not v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            AutoRaid = false
                            Mastery = true 
                        elseif CheckLevel == 1525 and v.Level.Value >= 250 and v.AwakenedMoves:FindFirstChild("V") then
                            AFM = false
                            autosuperhuman = false
                            Mastery = false
                            AutoRaid = false
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                        end
                    end
                end
            end
        end
    end)
-- ==== Full AutoFarm LevelMax + Mastery + Raid ====

-- ==== Full AutoFarm LevelMax ====
    spawn(function()
        while wait() do 
            wait(2)
            if FullLevelMax then
                local CheckLevel = game.Players.LocalPlayer.Data.Level.Value
                if CheckLevel == 1525 then 
                    AFM = false
                    autosuperhuman = false
                    Mastery = false
                    AutoRaid = false
                    game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nLevel Max !")
                end
            end
        end
    end)
-- ==== Full AutoFarm LevelMax ====

-- ==== Full AutoFarm Level700 ====
    spawn(function()
        while wait() do 
            wait(2)
            if FullLevel700 then
                local CheckLevel = game.Players.LocalPlayer.Data.Level.Value
                if CheckLevel >= 700 then 
                    AFM = false
                    autosuperhuman = false
                    Mastery = false
                    AutoRaid = false
                    game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nLevel 700 !")
                end
            end
        end
    end)
-- ==== Full AutoFarm Level700 ====

-- ==== AutoFarm ====-
    spawn(function()
        while wait() do
            if AFM then
                if LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                    CheckQuest()
                    LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest

                    wait(1.5)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
                elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                    CheckQuest()
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                    if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                        pcall(
                            function()
                                wait()
                                repeat wait()
                                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == Ms then
                                            CheckQuest()
                                            if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                                                for i,v in pairs(toweapon) do
                                                    EquipWeapon(v)
                                                end
                                                
                                                v.HumanoidRootPart.Size = Vector3.new(60, 5, 60)
                                                game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                                                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0)
                                                PosMon = v.HumanoidRootPart.CFrame
                                                v.HumanoidRootPart.CanCollide = false
                                            else
                                                CheckQuest()
                                                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                                            end
                                        end
                                    end
                                until LocalPlayer.PlayerGui.Main.Quest.Visible == false or AFM == false
                            end
                        )
                    else
                        CheckQuest()
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                    end 
                end
            end
        end
    end)
-- ==== AutoFarm ====

-- ==== ตีม้อน ====
    spawn(function()
        while wait() do
            if AFM then
                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if v.Name == Ms then
                        VirtualUser:CaptureController()
                        VirtualUser:ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
                    end
                end
            end
        end
    end)
-- ==== ตีม้อน ====

-- ==== ดึงม้อน ====
    local distanceNewworld = 300
    local distanceOldWorld = 150
    spawn(function()
        while wait() do
            if AFM then
                CheckQuest()
                pcall(
                    function()
                        repeat
                            if newworld then
                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == Ms and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= distanceNewworld then
                                        v.HumanoidRootPart.CFrame = PosMon
                                    end
                                end
                            end
                            if OldWorld then
                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == Ms and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= distanceOldWorld then
                                        v.HumanoidRootPart.CFrame = PosMon
                                    end
                                end
                            end
                        until LocalPlayer.PlayerGui.Main.Quest.Visible == false or not AFM  or not AutoRaidSuperHuman
                    end
                )
            end 
        end
    end)
-- ==== ดึงม้อน ====

-- ==== AutoNewWord ====
    spawn(function()
        while wait() do 
            local CheckLevel = game.Players.LocalPlayer.Data.Level.Value
            local Boss = "Ice Admiral [Lv. 700] [Boss]"
            local CFrameBoss700 = CFrame.new(1349.89917, 37.3493118, -1325.09839, 0.454798371, -4.58244607e-08, 0.890594423, 1.17673e-08, 1, 4.54446045e-08, -0.890594423, -1.01882405e-08, 0.454798371)
            local CFrameBoss = CFrame.new(1266.08948, 26.1765957, -1399.58069, -0.573598981, 0, -0.819136262, 0, 1, 0, 0.819136262, 0, -0.573598981)
            
            if AutoNewWord then
                if OldWorld then
                    if CheckLevel >= 800 then
                        AFM = false
                        local args = {
                            [1] = "DressrosaQuestProgress",
                            [2] = "Detective"
                        }
                        
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                            for o,t in pairs(toweapon) do
                                if v.Name == t then
                                    v.Parent = game.Players.LocalPlayer.Backpack
                                end
                            end
                        end
                        wait(3)
                        for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                            if v.Name == "Key" then
                                v.Parent = game.Players.LocalPlayer.Character
                                for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                                    if v.Name == "Key" then
                                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameBoss700
                                    end
                                end
                            end
                        end
                        wait(2)
                        AutoBoss = true
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameBoss700
                        while wait() do
                            if AutoBoss then
                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == Boss then
                                        if game:GetService("Workspace").Enemies:FindFirstChild(Boss) then
                                            
                                            for o,t in pairs(toweapon) do
                                                EquipWeapon(t)
                                            end
                                            
                                            v.HumanoidRootPart.Size = Vector3.new(60, 5, 60)
                                            game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                                            VirtualUser:CaptureController()
                                            VirtualUser:ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
                                            -- µÕàÍ§
                                            
                                            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 15, 15)
                                        else
                                            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameBoss
                                        end
                                    end
                                end
                            end
                        end
                    elseif FullLevel700 and CheckLevel >= 700 then
                        AFM = false
                        local args = {
                            [1] = "DressrosaQuestProgress",
                            [2] = "Detective"
                        }
                        
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                            for o,t in pairs(toweapon) do
                                if v.Name == t then
                                    v.Parent = game.Players.LocalPlayer.Backpack
                                end
                            end
                        end
                        wait(3)
                        for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                            if v.Name == "Key" then
                                v.Parent = game.Players.LocalPlayer.Character
                                for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                                    if v.Name == "Key" then
                                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameBoss700
                                    end
                                end
                            end
                        end
                        wait(2)
                        AutoBoss = true
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameBoss700
                        while wait() do
                            if AutoBoss then
                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == Boss then
                                        if game:GetService("Workspace").Enemies:FindFirstChild(Boss) then
                                            
                                            for o,t in pairs(toweapon) do
                                                EquipWeapon(t)
                                            end
                                            
                                            v.HumanoidRootPart.Size = Vector3.new(60, 5, 60)
                                            game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                                            VirtualUser:CaptureController()
                                            VirtualUser:ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
                                            -- µÕàÍ§
                                            
                                            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 15, 15)
                                        else
                                            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameBoss
                                        end
                                    end
                                end
                            end
                        end
                    end
                elseif newworld then
                    AutoNewWord = false
                end
                wait(5)
            end
        end
    end)
    spawn(function()
        while wait() do 
            if AutoNewWord then
                wait(5)
                if OldWorld then
                    local args = {
                        [1] = "TravelDressrosa"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
            end
        end
    end)
-- ==== AutoNewWord ====

-- ==== AutoStatus ====
    spawn(function()
        while wait() do
            if AFM then
                local StatsPoints = game.Players.LocalPlayer.Data.Points.Value
                local StatsMelee = game.Players.LocalPlayer.Data.Stats.Melee.Level.Value
                local StatsDefense = game.Players.LocalPlayer.Data.Stats.Defense.Level.Value
                if StatsMelee == 1525 then
                    if StatsDefense < 1525 then
                        local args = {
                            [1] = "AddPoint",
                            [2] = "Defense",
                            [3] = 1
                        }
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    end
                elseif StatsMelee < 1525 then
                    local args = {
                        [1] = "AddPoint",
                        [2] = "Melee",
                        [3] = 1
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if StatsMelee == 1525 and StatsDefense == 1525 then
                    local args = {
                        [1] = "AddPoint",
                        [2] = "Demon Fruit",
                        [3] = 1
                    }
            
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                wait(1)
            end
        end
    end)
-- ==== AutoStatus ====

-- ==== เปิดฮาคิเกราะ ====
    local OpenHaki = ""
    spawn(function()
        while wait() do 
            if AFM then
                for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                        if v.Name == "HasBuso" then
                            OpenHaki = v.Name
                            break
                        else
                            OpenHaki = v.Name
                        end
                end
                if OpenHaki ~= "HasBuso" then
                    local args = {
                        [1] = "Buso"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
                end
            end
            wait(5)
        end
    end)
-- ==== เปิดฮาคิเกราะ ====

-- ==== autodaedQuest ====
    valuemonster = ""
    spawn(function()
        while wait() do
            if AFM then 
                CheckQuest()
                if valuemonster ~= Ms then 
                    valuemonster = Ms
                    local args = {
                        [1] = "AbandonQuest"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
            end
            wait(5) 
        end
    end)
-- ==== autodaedQuest ====

--** ==== autosuperhuman // AutoRaid ====
    spawn(function()
        while wait() do 
            local CheckLevel = game.Players.LocalPlayer.Data.Level.Value
            if autosuperhuman then
                if not AutoRaidSuperHuman then
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        wait(2)
                        if v.Name == "Fishman Karate" and v.Level.Value >= 300 and CheckLevel >= 1100 then
                            AFM = false
                            RaidBuyChip()
                            AutoRaidSuperHuman = true
                        elseif v.Name == "Dragon Claw" then
                            AFM = true
                            AutoRaidSuperHuman = false
                        end
                    end
                    for i, v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                        wait(2)
                        if v.Name == "Fishman Karate" and v.Level.Value >= 300 and CheckLevel >= 1100 then
                            AFM = false
                            RaidBuyChip()
                            AutoRaidSuperHuman = true
                        elseif v.Name == "Dragon Claw" then
                            AFM = true
                            AutoRaidSuperHuman = false
                        end
                    end
                end
                wait(1)
            end
        end
    end)
    -- ==== Raid + ServerHop ====
    spawn(function()
        while wait() do
            if AutoRaid then
                wait(1)
                checkfruits = game:GetService("Players").localPlayer.Data.DevilFruit.Value
                for i,v in pairs(game:GetService("Players").localPlayer.Backpack:GetChildren()) do
                    if v.Name == checkfruits then
                        if _G.lookAwake and v.AwakenedMoves:FindFirstChild("V") then
                            print("สำเร็จ ผลตื่นหมดแล้ว")
                            OldLevel = game.Players.localPlayer.Data.Level.Value
                            game.Players.localPlayer:Kick("\n Auto Fram Completed Level : "..game.Players.localPlayer.Data.Level.Value.."\nUsername : "..game.Players.LocalPlayer.Name.."\nFruit Awakeall")
                            AutoRaidHop = false
                            AutoRaid = false
                        end
                    end
                end
                wait(2)
                local CheckF = ""
                for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                    CheckF = v.Name
                end
                if not AutoRaidHop then 
                    if string.find(CheckF, "Fruit") then 
                        wait(0.5)
                        BuyChip()
                        wait(0.5)
                        fireclickdetector(game:GetService("Workspace").Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                        wait(0.5)
                        AutoRaidHop = true
                    else
                        Teleport()
                    end
                end
            end
        end
    end)
    -- ==== Raid  ====
    spawn(function()
        while wait() do 
            if raid then 
                if not AutoRaidRoom then 
                    RaidBuyChip()
                    AutoRaidRoom = true
                    wait(2)
                end 
            end 
            wait(1)
        end
    end)
    -- ==== CheckFragments ====
    SuperHMCheckFmt = game.Players.LocalPlayer.Data.Fragments.Value 
    spawn(function()
        while wait() do
            local SuperHMCheckFm = game.Players.LocalPlayer.Data.Fragments.Value 
            if AutoRaidSuperHuman or AutoRaidHop or AutoRaidRoom then
                if SuperHMCheckFm ~= SuperHMCheckFmt then 
                    SuperHMCheckFmt = SuperHMCheckFm
                    AutoRaidSuperHuman = false
                    AutoRaidHop = false
                    AutoRaidRoom = false
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-146.680069, 75.8651886, 2835.68945, 0.999935508, -1.36373113e-09, -0.01134797, 9.34709421e-10, 1, -3.78101674e-08, 0.01134797, 3.77971148e-08, 0.999935508)

                end
                wait(2)
            end
        end
    end)
    -- ==== AutoRaidSuperHuman ====
    spawn(function()
        while wait() do 
            repeat wait()
                if AutoRaidSuperHuman or AutoRaidHop or AutoRaidRoom then
                    game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                    if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                        if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").CFrame*CFrame.new(0,40,0)
                            
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").CFrame*CFrame.new(0,40,0)
                            
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").CFrame*CFrame.new(0,40,0)
                            
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").CFrame*CFrame.new(0,40,0)
                            
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").CFrame*CFrame.new(0,40,0)
                            
                        end
                    else                
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-146.680069, 75.8651886, 2835.68945, 0.999935508, -1.36373113e-09, -0.01134797, 9.34709421e-10, 1, -3.78101674e-08, 0.01134797, 3.77971148e-08, 0.999935508)
                        
                    end 
                end
            until not AutoRaidSuperHuman or not AutoRaidHop or not AutoRaidRoom
        end
    end)
    -- ==== Kill All ====
    spawn(function()
        while wait() do 
            if AutoRaidSuperHuman or AutoRaidHop or AutoRaidRoom then
                for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 4000 then
                        pcall(function()
                            repeat wait()
                                v.HumanoidRootPart.Size = Vector3.new(50, 50, 50)
                                v.HumanoidRootPart.CanCollide = false
                                v.Humanoid.Health = 0
                            until not AutoRaidSuperHuman or not v.Parent or v.Humanoid.Health <= 0 or not AutoRaidHop or not AutoRaidRoom
                        end)
                    end
                end
            end
        end
    end)
    -- ==== Buy Chip SuperHuman ====
    function RaidBuyChip()
        if not AutoRaidSuperHuman then 
            fruits = "Light"
            local args = {
                [1] = "RaidsNpc",
                [2] = "Select",
                [3] = fruits
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            wait(2)
            local args1 = {
                [1] = "Cousin",
                [2] = "Buy"
            }
            
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args1))
            wait(1)
            fireclickdetector(game:GetService("Workspace").Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
        end
    end
    -- ==== Buy Chip AutoRaid
    fruits = ""
    function BuyChip()
        if not AutoRaidHop or not AutoRaidRoom then
            checkfruits = game:GetService("Players").localPlayer.Data.DevilFruit.Value
            if checkfruits == "Flame-Flame" then
                fruits = "Flame"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            elseif checkfruits == "Ice-Ice" then
                fruits = "Ice"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            elseif checkfruits == "Quake-Quake" then
                fruits = "Quake"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            elseif checkfruits == "Light-Light" then
                fruits = "Light"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            elseif checkfruits == "Dark-Dark" then
                fruits = "Dark"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            elseif checkfruits == "String-String" then
                fruits = "String"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            elseif checkfruits == "Rumble-Rumble" then
                fruits = "Rumble"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            elseif checkfruits == "" then
                fruits = "Light"
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = fruits
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end
    -- ==== CheckHP AutoRaid ====
    spawn(function()
        while wait() do
            wait(0.5)
            if AutoRaidSuperHuman or AutoRaidHop or AutoRaidRoom then
                local CheckHP = game.Players.LocalPlayer.Character.Humanoid
                if CheckHP.Health <= 0 then
                    wait(1)        
                    AutoRaidSuperHuman = false
                    AutoRaidHop = false
                    AutoRaidRoom = false
                end
            end
        end
    end)
    -- ==== TimeCheck AutoRaid ====
    spawn(function()
        while wait() do
            wait(0.5)
            if AutoRaidSuperHuman or AutoRaidHop or AutoRaidRoom then
                wait(20)        
                game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                if not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") or
                    not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") or
                    not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") or
                    not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") or
                    not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                    AutoRaidSuperHuman = false
                    AutoRaidHop = false
                    AutoRaidRoom = false
                    print("รีAutoRaid")
                end
            end
        end
    end)
    -- ==== BringFruit ====
    spawn(function() 
        while wait() do 
            if AutoRaid then
                for i,v in pairs(game.Workspace:GetChildren()) do
                    if v:IsA("Tool") then
                        v.Handle.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                        wait(1)
                        for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                            if v:IsA("Tool") then 
                                v.Parent = game.Players.LocalPlayer.Backpack
                            end
                        end
                    end
                end
            end
        end
    end)
    -- ==== AwaKen ====
    spawn(function()
        while wait() do
            if AutoRaid or room1 or room2 or room3 then
                wait(3)
                local args = {
                    [1] = "Awakener",
                    [2] = "Awaken"
                }
    
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end)
    -- ==== ReConnect ====
    spawn(function()
        while wait() do
            if AutoRaid then
                checkfruits = game:GetService("Players").localPlayer.Data.DevilFruit.Value
                for i,v in pairs(game:GetService("Players").localPlayer.Backpack:GetChildren()) do
                    wait(5)
                    if v.Name == checkfruits then
                        if _G.lookAwake and not v.AwakenedMoves:FindFirstChild("V") then
                            game.NetworkClient.ChildRemoved:Connect(function()
                                game:GetService('TeleportService'):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
                            end)
                        end
                    end
                end
                for i,v in pairs(game:GetService("Players").localPlayer.Character:GetChildren()) do
                    wait(5)
                    if v.Name == checkfruits then
                        if _G.lookAwake and not v.AwakenedMoves:FindFirstChild("V") then
                            game.NetworkClient.ChildRemoved:Connect(function()
                                game:GetService('TeleportService'):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
                            end)
                        end
                    end
                end
            end
            wait(5)
        end
    end)
--** ==== autosuperhuman ====

-- ==== Room 1 - 2 - 3 ====
    spawn(function() 
        while wait() do     
            if room1 then 
                repeat wait()
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6504.1626, 249.531662, -4482.6416, 0.522245646, -3.05290939e-08, -0.852794945, 9.56429318e-08, 1, 2.27721948e-08, 0.852794945, -9.34564994e-08, 0.522245646)
                    wait()
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6432.65332, 255.60675, -4488.69434, -0.999392271, 0, 0.0348687991, 0, 1, 0, -0.0348687991, 0, -0.999392271)
                    wait(5)
                until room1 == false
            end
            
            if room2 then 
                repeat wait()
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6504.1626, 249.531662, -4482.6416, 0.522245646, -3.05290939e-08, -0.852794945, 9.56429318e-08, 1, 2.27721948e-08, 0.852794945, -9.34564994e-08, 0.522245646)
                    wait()
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6437.14307, 255.60675, -4474.70166, -0.999392271, 0, 0.0348687991, 0, 1, 0, -0.0348687991, 0, -0.999392271)
                    wait(5)
                until room2 == false
            end
            
            if room3 then 
                repeat wait()
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6504.1626, 249.531662, -4482.6416, 0.522245646, -3.05290939e-08, -0.852794945, 9.56429318e-08, 1, 2.27721948e-08, 0.852794945, -9.34564994e-08, 0.522245646)
                    wait()
                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6444.63135, 255.60675, -4460.71094, -0.999392271, 0, 0.0348687991, 0, 1, 0, -0.0348687991, 0, -0.999392271)
                    wait(5)
                until room3 == false
            end
        end
    end)
-- ==== Room 1 - 2 - 3 ====

--** ==== AutoMastery Devil Fruit ====
    spawn(function()
        while wait() do
            if Mastery then
                if LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                    CheckQuest()
                    LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
                    wait(1.1)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
                elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                    CheckQuest()
                    LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                    if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                        pcall(function()
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                CheckQuest()  
                                if v.Name == Ms then
                                    repeat wait() CheckQuest()  
                                        if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                                            if string.find(LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
                                                HealthMin = v.Humanoid.MaxHealth*10/100
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if v.Humanoid.Health <= HealthMin then
                                                    EquipWeapon(game.Players.LocalPlayer.Data.DevilFruit.Value)
                                                    v.HumanoidRootPart.CanCollide = false
                                                    v.HumanoidRootPart.Size = Vector3.new(60, 5, 60)
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,20,20)
                                                else
                                                    for i,v in pairs(toweapon) do
                                                        EquipWeapon(v)
                                                    end
                                                    v.HumanoidRootPart.CanCollide = false
                                                    v.HumanoidRootPart.Size = Vector3.new(60, 5, 60)
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,20,20)
                                                    game:GetService'VirtualUser':CaptureController()
                                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))  
                                                end
                                            else
                                                CheckQuest()
                                                LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                                                wait(1.5)
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
                                            end  
                                        else
                                            CheckQuest() 
                                            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                                        end 
                                    until not v.Parent or v.Humanoid.Health <= 0  or LocalPlayer.PlayerGui.Main.Quest.Visible == false or Mastery == false
                                    CheckQuest() 
                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                                end
                            end
                        end)
                    else
                        CheckQuest()
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                    end 
                end
            end
        end
    end)
    spawn(function()
        while wait() do
            if Mastery then
                pcall(function()
                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        CheckQuest()  
                        if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                            if string.find(LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
                                HealthMin = v.Humanoid.MaxHealth*10/100
                                if v.Humanoid.Health <= HealthMin then
                                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dragon-Dragon") then
                                        if  v.Humanoid.Health <= HealthMin then
                                            local args = {
                                                [1] = v.HumanoidRootPart.Position
                                            }
                                            game:GetService("Players").LocalPlayer.Character["Dragon-Dragon"].RemoteEvent:FireServer(unpack(args))
                                            local args = {
                                                [1] = "Z",
                                                [2] = Vector3.new(0,0,0)
                                            }
                                            game:GetService("Players").LocalPlayer.Character["Dragon-Dragon"].RemoteFunction:InvokeServer(unpack(args))
                                        end
                                        if  v.Humanoid.Health <= HealthMin then
                                            local args = {
                                                [1] = v.HumanoidRootPart.Position
                                            }
                                            game:GetService("Players").LocalPlayer.Character["Dragon-Dragon"].RemoteEvent:FireServer(unpack(args))
                                            local args = {
                                                [1] = "X"
                                            }
                                            game:GetService("Players").LocalPlayer.Character["Dragon-Dragon"].RemoteFunction:InvokeServer(unpack(args))
                                        end   
                                    elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value) then
                                        if v.Humanoid.Health <= HealthMin then
                                            local args = {
                                                [1] = v.HumanoidRootPart.Position
                                            }
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteEvent:FireServer(unpack(args))
                                            local args = {
                                                [1] = "Z",
                                                [2] = Vector3.new(0,0,0)
                                            }
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteFunction:InvokeServer(unpack(args))
                                        end
                                        if v.Humanoid.Health <= HealthMin then
                                            local args = {
                                                [1] = v.HumanoidRootPart.Position
                                            }
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteEvent:FireServer(unpack(args))
                                            local args = {
                                                [1] = "X",
                                                [2] = Vector3.new(0,0,0)
                                            }
                                            
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteFunction:InvokeServer(unpack(args))
                                        end
                                        if v.Humanoid.Health <= HealthMin then
                                            local args = {
                                                [1] = v.HumanoidRootPart.Position
                                            }
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteEvent:FireServer(unpack(args))
                                            local args = {
                                                [1] = "C",
                                                [2] = Vector3.new(0,0,0)
                                            }
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteFunction:InvokeServer(unpack(args))
                                        end
                                        if v.Humanoid.Health <= HealthMin then
                                            local args = {
                                                [1] = v.HumanoidRootPart.Position
                                            }
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteEvent:FireServer(unpack(args))
                                            local args = {
                                                [1] = "V",
                                                [2] = Vector3.new(0,0,0)
                                            }
                                            game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Data.DevilFruit.Value].RemoteFunction:InvokeServer(unpack(args))
                                        end
                                    end   
                                end
                            end
                        end
                    end
                end)
            end
        end
    end)
--** ==== AutoMastery Devil Fruit ====

-- ==== AutoMastery Gun ====
    function AutoGunMastery()
        if game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false then  
        CheckQuest()
        print()
        LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
        wait(1.1)
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
        wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
        elseif game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == true then  
        for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
        CheckQuest()
                pcall(function()
                    if game.Workspace.Enemies:FindFirstChild(Ms) then
                    if GunMastery and v.Name == Ms then
                        repeat wait()
                            pcall(function()
                                if game.Workspace.Enemies:FindFirstChild(Ms) then
                                    if string.find(LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
                                        PosMon = v.HumanoidRootPart.CFrame
                                        EquipWeapon(WeaponMastery)
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(60, 5, 60)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,20,0)
                                        game:GetService'VirtualUser':CaptureController()
                                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    else
                                    CheckQuest()
                                    LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
                                    wait(1.1)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
                                    wait(0.5)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                                    end
                                else
                                CheckQuest()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                                end
                            end)
                        until game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false or GunMastery == false or v.Humanoid.Health <= 0 or not v.Parent
                    end
                    else
                    CheckQuest()
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                    end
                end)
            end
        end
    end
-- ==== AutoMastery Gun ====

-- ==== autosuperhuman ====
    spawn(function()
        while wait() do
            if autosuperhuman then
                pcall(function()
                    local checkbeli = game.Players.LocalPlayer.Data.Beli.Value 
                    local CheckFragments = game.Players.LocalPlayer.Data.Fragments.Value 
                    for i, v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
                        if v.Name == "Combat" then
                            if checkbeli >= 150000 then
                                local args = {
                                    [1] = "BuyBlackLeg"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                
                                for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                    for o,t in pairs(toweapon) do
                                        if v.Name == t then
                                            v.Parent = game.Players.LocalPlayer.Character
                                        end
                                    end
                                end
                            end
                        elseif v.Name == "Black Leg" and v.Level.Value >= 300 then
                            local args = {
                                [1] = "BuyElectro"
                            }
                            
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Character
                                    end
                                end
                            end
                        elseif v.Name == "Electro" and v.Level.Value >= 300 then
                            local args = {
                                [1] = "BuyFishmanKarate"
                            }
                            
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Character
                                    end
                                end
                            end
                        elseif v.Name == "Fishman Karate" and v.Level.Value >= 300 and CheckFragments >= 1500 then
                            local args = {
                                [1] = "BlackbeardReward",
                                [2] = "DragonClaw",
                                [3] = "1"
                            }
                    
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            local args = {
                                [1] = "BlackbeardReward",
                                [2] = "DragonClaw",
                                [3] = "2"
                            }
                    
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Backpack
                                    end
                                end
                            end
                        elseif v.Name == "Dragon Claw" and v.Level.Value >= 300 then
                            local args = {
                                [1] = "BuySuperhuman"
                            }
                            
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Character
                                    end
                                end
                            end
                        end
                    end
                    for i, v in pairs(game:GetService("Players").LocalPlayer.Character:GetChildren()) do
                        if v.Name == "Combat" then
                            if checkbeli >= 150000 then
                                local args = {
                                    [1] = "BuyBlackLeg"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                
                                for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                    for o,t in pairs(toweapon) do
                                        if v.Name == t then
                                            v.Parent = game.Players.LocalPlayer.Character
                                        end
                                    end
                                end
                            end
                        elseif v.Name == "Black Leg" and v.Level.Value >= 300 then
                            local args = {
                                [1] = "BuyElectro"
                            }
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Character
                                    end
                                end
                            end
                        elseif v.Name == "Electro" and v.Level.Value >= 300 then
                            local args = {
                                [1] = "BuyFishmanKarate"
                            }
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Character
                                    end
                                end
                            end
                        elseif v.Name == "Fishman Karate" and v.Level.Value >= 300 and CheckFragments >= 1500 then
                            local args = {
                                [1] = "BlackbeardReward",
                                [2] = "DragonClaw",
                                [3] = "1"
                            }
                    
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            local args = {
                                [1] = "BlackbeardReward",
                                [2] = "DragonClaw",
                                [3] = "2"
                            }
                    
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Backpack
                                    end
                                end
                            end
                        elseif v.Name == "Dragon Claw" and v.Level.Value >= 300 then
                            local args = {
                                [1] = "BuySuperhuman"
                            }
                            
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                                for o,t in pairs(toweapon) do
                                    if v.Name == t then
                                        v.Parent = game.Players.LocalPlayer.Character
                                    end
                                end
                            end
                        end
                    end
                end)
            end
            wait(5)
        end
    end)
-- ==== autosuperhuman ====

-- ==== All ====
    spawn(function()
        while wait() do
            if AFM then 
                Haki()
                Redeem()
                LegendarySword()
                BuyFruits()
                SuperHuman()
            end
            wait(300)
        end
    end)
    function Haki()
        local CheckBeli = game.Players.LocalPlayer.Data.Beli.Value 
        if CheckBeli >= 10000 then
            local HakiGeppo = {
                [1] = "BuyHaki",
                [2] = "Geppo"
            }

            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(HakiGeppo))
        end
        if CheckBeli >= 25000 then

            local HakiBuso = {
                [1] = "BuyHaki",
                [2] = "Buso"
            }

            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(HakiBuso))
        end
        if CheckBeli >= 100000 then
            local HakiSoru = {
                [1] = "BuyHaki",
                [2] = "Soru"
            }

            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(HakiSoru))
            AutoHaki = false
        end
    end
    function Redeem()
        pcall(
            function()
                local CheckLevel = game.Players.LocalPlayer.Data.Level.Value
                if CheckLevel >= _G.AutoRedeemCode then
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("SUB2GAMERROBOT_EXP1")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("StrawHatMaine")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("Sub2OfficialNoobie")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("THEGREATACE")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("SUB2NOOBMASTER123")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("Sub2Daigrock")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("Axiore")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("TantaiGaming")
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer("STRAWHATMAINE")
                end
            end
        )
    end
    function LegendarySword()
        local args = {
            [1] = "LegendarySwordDealer",
            [2] = "1"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        local args = {
            [1] = "LegendarySwordDealer",
            [2] = "2"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        local args = {
            [1] = "LegendarySwordDealer",
            [2] = "3"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        local args = {
            [1] = "OpenRengoku"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        local args = {
            [1] = "Ectoplasm",
            [2] = "Buy",
            [3] = 3
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end
    function BuyFruits()
        local CheckFruits = game.Players.localPlayer.Data.DevilFruit.Value
        local fruits = {
            [1] = _G.Fruits1,
            [2] = _G.Fruits2,
            [3] = _G.Fruits3,
            [4] = _G.Fruits4,
            [5] = _G.Fruits5,
            [6] = _G.Fruits6
        }
        if CheckFruits == "" then
            game:GetService("Players").LocalPlayer.PlayerGui.Main.FruitShop.Visible = true
            for i,v in pairs(fruits) do
                local args = {
                    [1] = "PurchaseRawFruit",
                    [2] = v
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
            game:GetService("Players").LocalPlayer.PlayerGui.Main.FruitShop.Visible = false
        end
    end
-- ==== All ====

-- ==== Anti AFK ====
    spawn(function()
        while wait() do 
            local VirtualUser=game:service'VirtualUser'
            game:service'Players'.LocalPlayer.Idled:connect(function()
                VirtualUser:CaptureController()
                VirtualUser:ClickButton2(Vector2.new())
            end)
            wait(60)
        end 
    end)
-- ==== Anti AFK ====

-- ==== Server Hop ====
    local PlaceID = game.PlaceId
    local AllIDs = {}
    local foundAnything = ""
    local actualHour = os.date("!*t").hour
    local Deleted = false
    local File = pcall(function()
        AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
    end)
    if not File then
        table.insert(AllIDs, actualHour)
        writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
    end
    function TPReturner()
        local Site;
        if foundAnything == "" then
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
        else
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
        end
        local ID = ""
        if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
            foundAnything = Site.nextPageCursor
        end
        local num = 0;
        for i,v in pairs(Site.data) do
            local Possible = true
            ID = tostring(v.id)
            if tonumber(v.maxPlayers) > tonumber(v.playing) then
                for _,Existing in pairs(AllIDs) do
                    if num ~= 0 then
                        if ID == tostring(Existing) then
                            Possible = false
                        end
                    else
                        if tonumber(actualHour) ~= tonumber(Existing) then
                            local delFile = pcall(function()
                                delfile("NotSameServers.json")
                                AllIDs = {}
                                table.insert(AllIDs, actualHour)
                            end)
                        end
                    end
                    num = num + 1
                end
                if Possible == true then
                    table.insert(AllIDs, ID)
                    wait()
                    pcall(function()
                        writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                        wait()
                        game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                    end)
                    wait(4)
                end
            end
        end
    end

    function Teleport()
        while wait() do
            pcall(function()
                TPReturner()
                if foundAnything ~= "" then
                    TPReturner()
                end
            end)
        end
    end
-- ==== Server Hop ====
