--// This file was created by XHider https://discord.com/invite/E2N7w35zkt

local G = {};
G.listfunction = {};
G.listtab = {};
local M = game.Players.LocalPlayer.PlayerGui:FindFirstChild("TouchGui");
local X;
local I;
local Y;
local u = {};
local P = {
		["Border Color"] = Color3.fromRGB(0, 255, 255),
		["Click Effect Color"] = Color3.fromRGB(230, 230, 230),
		["Setting Icon Color"] = Color3.fromRGB(230, 230, 230),
		["Logo Image"] = "rbxassetid://deoco",
		["Search Icon Color"] = Color3.fromRGB(255, 255, 255),
		["Search Icon Highlight Color"] = Color3.fromRGB(0, 255, 255),
		["GUI Text Color"] = Color3.fromRGB(230, 230, 230),
		["Text Color"] = Color3.fromRGB(230, 230, 230),
		["Placeholder Text Color"] = Color3.fromRGB(178, 178, 178),
		["Title Text Color"] = Color3.fromRGB(0, 255, 255),
		["Background Main Color"] = Color3.fromRGB(15, 15, 15),
		["Background 1 Color"] = Color3.fromRGB(28, 28, 34),
		["Background 1 Transparency"] = .25,
		["Background 2 Color"] = Color3.fromRGB(90, 90, 90),
		["Background 3 Color"] = Color3.fromRGB(20, 20, 20),
		["Background Image"] = "",
		["Page Selected Color"] = Color3.fromRGB(0, 255, 255),
		["Section Text Color"] = Color3.fromRGB(0, 255, 255),
		["Section Underline Color"] = Color3.fromRGB(0, 255, 255),
		["Toggle Border Color"] = Color3.fromRGB(0, 255, 255),
		["Toggle Checked Color"] = Color3.fromRGB(230, 230, 230),
		["Toggle Desc Color"] = Color3.fromRGB(185, 185, 185),
		["Button Color"] = Color3.fromRGB(35, 35, 35),
		["Label Color"] = Color3.fromRGB(35, 35, 35),
		["Dropdown Icon Color"] = Color3.fromRGB(230, 230, 230),
		["Dropdown Selected Color"] = Color3.fromRGB(0, 255, 255),
		["Dropdown Selected Check Color"] = Color3.fromRGB(0, 255, 255),
		["Textbox Highlight Color"] = Color3.fromRGB(0, 255, 255),
		["Box Highlight Color"] = Color3.fromRGB(0, 255, 255),
		["Slider Line Color"] = Color3.fromRGB(45, 22, 67),
		["Slider Highlight Color"] = Color3.fromRGB(0, 255, 255),
		["Tween Animation 1 Speed"] = M and 0 or .25,
		["Tween Animation 2 Speed"] = M and 0 or .5,
		["Tween Animation 3 Speed"] = M and 0 or .1,
		["Text Stroke Transparency"] = .5,
	};
G.UIColor = P;
G.UIToggled = false;
local s = {};
local w = {};
local r = {};
local C = game:GetService("TweenService");
local A = game:GetService("UserInputService");
local R = game:GetService("RunService");
local function m(G, X)
	local I = nil;
	local Y = nil;
	local u = nil;
	local P = nil;
	G.InputBegan:Connect(function(G)
		if G.UserInputType == Enum.UserInputType.MouseButton1 or G.UserInputType == Enum.UserInputType.Touch then
			I = true;
			u = G.Position;
			P = X.Position;
			G.Changed:Connect(function()
				if G.UserInputState == Enum.UserInputState.End then
					I = false;
				end;
			end);
		end;
	end);
	G.InputChanged:Connect(function(G)
		if G.UserInputType == Enum.UserInputType.MouseMovement or G.UserInputType == Enum.UserInputType.Touch then
			Y = G;
		end;
	end);
	A.InputChanged:Connect(function(G)
		if G == Y and I then
			local I = G.Position - u;
			if not djtmemay and cac then
				(C:Create(X, TweenInfo.new(M and 0 or .35, Enum.EasingStyle.Linear, Enum.EasingDirection.Out), { Position = UDim2.new(P.X.Scale, P.X.Offset + I.X, P.Y.Scale, P.Y.Offset + I.Y) })):Play();
			elseif not djtmemay and not cac then
				X.Position = UDim2.new(P.X.Scale, P.X.Offset + I.X, P.Y.Scale, P.Y.Offset + I.Y);
			end;
		end;
	end);
end;
r.Gui = Instance.new("ScreenGui");
r.Gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling;
r.Gui.Name = "noguchihyuga";
r.Gui.Enabled = false;
G.ReadyForGuiLoaded = false;
spawn(function()
	repeat
		task.wait();
	until G.ReadyForGuiLoaded;
	if G.UIToggled then
		r.Gui.Enabled = true;
	end;
end);
r.NotiGui = Instance.new("ScreenGui");
r.NotiGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling;
r.NotiGui.Name = "noguchi.hyuga Notification";
r.HideGui = Instance.new("ScreenGui");
r.HideGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling;
r.HideGui.Name = "noguchi.hyuga Btn";
local f = Instance.new("Frame");
local t = Instance.new("UIListLayout");
f.Name = "NotiContainer";
f.Parent = r.NotiGui;
f.AnchorPoint = Vector2.new(1, 1);
f.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
f.BackgroundTransparency = 1.0;
f.Position = UDim2.new(1, -5, 1, -5);
f.Size = UDim2.new(0, 350, 1, -10);
t.Name = "NotiList";
t.Parent = f;
t.SortOrder = Enum.SortOrder.LayoutOrder;
t.VerticalAlignment = Enum.VerticalAlignment.Bottom;
t.Padding = UDim.new(0, 5);
r.Gui.Parent = game.Players.LocalPlayer.PlayerGui;
r.NotiGui.Parent = game.Players.LocalPlayer.PlayerGui;
r.HideGui.Parent = game.Players.LocalPlayer.PlayerGui;
local i = Instance.new("ImageButton", r.HideGui);
i.BorderSizePixel = 0;
i.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
i.AnchorPoint = Vector2.new(0, 1);
i.Image = "rbxassetid://NutDau";
i.Size = UDim2.new(0, 50, 0, 50);
i.BorderColor3 = Color3.fromRGB(0, 0, 0);
i.Position = UDim2.new(.01, 0, .99, 0);
m(i, i);
i.MouseButton1Down:Connect(function()
	r.Gui.Enabled = not r.Gui.Enabled;
end);
local D = Instance.new("UICorner", i);
D.CornerRadius = UDim.new(1, 8);
local p = Instance.new("UIStroke", i);
p.Thickness = .6;
p.Color = Color3.fromRGB(0, 255, 255);
function r.Getcolor(G)
	return { math.floor(G.r * 255), math.floor(G.g * 255), math.floor(G.b * 255) };
end;
local S = function(M)
		G.TitleNameNoti = M.Title or "";
		local X = M.Desc;
		local I = M.ShowTime or 10;
		local Y = Instance.new("Frame");
		local u = Instance.new("Frame");
		local P = Instance.new("UICorner");
		local s = Instance.new("Frame");
		local w = Instance.new("ImageLabel");
		local A = Instance.new("UICorner");
		local R = Instance.new("TextLabel");
		local m = Instance.new("Frame");
		local t = Instance.new("ImageLabel");
		local i = Instance.new("TextButton");
		local D = Instance.new("TextLabel");
		Y.Name = "NotiFrame";
		Y.Parent = f;
		Y.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		Y.BackgroundTransparency = 1.0;
		Y.ClipsDescendants = true;
		Y.Position = UDim2.new(0, 0, 0, 0);
		Y.Size = UDim2.new(1, 0, 0, 0);
		Y.AutomaticSize = Enum.AutomaticSize.Y;
		u.Name = "Noticontainer";
		u.Parent = Y;
		u.Position = UDim2.new(1, 0, 0, 0);
		u.Size = UDim2.new(1, 0, 1, 6);
		u.AutomaticSize = Enum.AutomaticSize.Y;
		u.BackgroundColor3 = Color3.fromRGB(48, 47, 55);
		P.CornerRadius = UDim.new(0, 4);
		P.Parent = u;
		s.Name = "Topnoti";
		s.Parent = u;
		s.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		s.BackgroundTransparency = 1.0;
		s.Position = UDim2.new(0, 0, 0, 5);
		s.Size = UDim2.new(1, 0, 0, 25);
		w.Name = "Ruafimg";
		w.Parent = s;
		w.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		w.BackgroundTransparency = 1.0;
		w.Position = UDim2.new(0, 5, 0, G.T1 and 5 or 0);
		w.Size = UDim2.new(0, G.T1 and 30 or 25, 0, G.T1 and 15 or 25);
		w.Image = G.UIColor["Logo Image"];
		A.CornerRadius = UDim.new(1, 0);
		A.Name = "RuafimgCorner";
		A.Parent = w;
		local p = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[1]);
		local S = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[2]);
		local U = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[3]);
		local b = p .. ("," .. (S .. ("," .. U)));
		R.Text = "<font color=\"rgb(" .. (b .. (")\">Long Béo Ú Hub</font> " .. G.TitleNameNoti));
		R.Name = "TextLabelNoti";
		R.Parent = s;
		R.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		R.BackgroundTransparency = 1.0;
		R.Position = UDim2.new(0, G.T1 and 40 or 35, 0, 0);
		R.Size = UDim2.new(1, G.T1 and -40 or -35, 1, 0);
		R.Font = Enum.Font.GothamBold;
		R.TextSize = 14.0;
		R.TextWrapped = true;
		R.TextXAlignment = Enum.TextXAlignment.Left;
		R.RichText = true;
		R.TextColor3 = G.UIColor["GUI Text Color"];
		m.Name = "CloseContainer";
		m.Parent = s;
		m.AnchorPoint = Vector2.new(1, .5);
		m.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		m.BackgroundTransparency = 1.0;
		m.Position = UDim2.new(1, -4, .5, 0);
		m.Size = UDim2.new(0, 22, 0, 22);
		t.Name = "CloseImage";
		t.Parent = m;
		t.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		t.BackgroundTransparency = 1.0;
		t.Size = UDim2.new(1, 0, 1, 0);
		t.Image = "rbxassetid://129781592728096";
		t.ImageRectOffset = Vector2.new(284, 4);
		t.ImageRectSize = Vector2.new(24, 24);
		t.ImageColor3 = G.UIColor["Search Icon Color"];
		i.Parent = m;
		i.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		i.BackgroundTransparency = 1.0;
		i.Size = UDim2.new(1, 0, 1, 0);
		i.Font = Enum.Font.FredokaOne;
		i.Text = "X";
		i.TextColor3 = Color3.fromRGB(0, 0, 0);
		i.TextSize = 14.0;
		i.FontFace = Font.new("rbxasset://fonts/families/FredokaOne.json", Enum.FontWeight.Bold, Enum.FontStyle.Normal);
		i.TextColor3 = Color3.new(1, 1, 1);
		if X then
			D.Name = "TextColor";
			D.Parent = u;
			D.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
			D.BackgroundTransparency = 1.0;
			D.Position = UDim2.new(0, 10, 0, 35);
			D.Size = UDim2.new(1, -15, 0, 0);
			D.Font = Enum.Font.GothamBold;
			D.Text = X;
			D.TextSize = 14.0;
			D.TextXAlignment = Enum.TextXAlignment.Left;
			D.RichText = true;
			D.TextColor3 = G.UIColor["Text Color"];
			D.AutomaticSize = Enum.AutomaticSize.Y;
			D.TextWrapped = true;
		end;
		local function F()
			(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { Position = UDim2.new(1, 0, 0, 0) })):Play();
			wait(.25);
			Y:Destroy();
		end;
		(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { Position = UDim2.new(0, 0, 0, 0) })):Play();
		i.MouseEnter:Connect(function()
			(C:Create(t, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { ImageColor3 = G.UIColor["Search Icon Highlight Color"] })):Play();
		end);
		i.MouseLeave:Connect(function()
			(C:Create(t, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { ImageColor3 = G.UIColor["Search Icon Color"] })):Play();
		end);
		i.MouseButton1Click:Connect(function()
			wait(.25);
			F();
		end);
		spawn(function()
			wait(I);
			F();
		end);
	end;
function w.CreateNoti(M, X)
	if not G.Config or X then
		local G, X = pcall(function()
				S(M);
			end);
		if X then
			rconsoleprint(X);
		end;
	end;
end;
function w.CreateMain(M)
	local X = "by vhai";
	G.MainDesc = M.Desc or "";
	local I = false;
	cac = false;
	local P = Instance.new("Frame");
	local s = Instance.new("ImageLabel");
	local w = Instance.new("UICorner");
	local A = Instance.new("Frame");
	local f = Instance.new("ImageLabel");
	local t = Instance.new("TextLabel");
	local i = Instance.new("Frame");
	local D = Instance.new("UICorner");
	local p = Instance.new("ScrollingFrame");
	local S = Instance.new("UIListLayout");
	local U = Instance.new("TextLabel");
	local b = Instance.new("Frame");
	local F = Instance.new("UIPageLayout");
	local j = Instance.new("Frame");
	local n = Instance.new("Frame");
	local c;
	P.Name = "Main";
	P.Parent = r.Gui;
	P.BackgroundColor3 = Color3.fromRGB(42, 42, 42);
	P.BackgroundTransparency = 1.0;
	P.Position = UDim2.new(.5, 0, .5, 0);
	P.AnchorPoint = Vector2.new(.5, .5);
	P.Size = UDim2.new(0, 629, 0, 359);
	m(P, P);
	s.Name = "maingui";
	s.Parent = P;
	s.AnchorPoint = Vector2.new(.5, .5);
	s.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
	s.BackgroundTransparency = 1.0;
	s.Position = UDim2.new(.5, 0, .5, 0);
	s.Selectable = true;
	s.Size = UDim2.new(1, 30, 1, 30);
	s.Image = "rbxassetid://129781592728096";
	s.ScaleType = Enum.ScaleType.Slice;
	s.SliceCenter = Rect.new(15, 15, 175, 175);
	s.SliceScale = 1.3;
	s.ImageColor3 = G.UIColor["Border Color"];
	s.ImageTransparency = 1;
	s.ImageColor3 = G.UIColor["Title Text Color"];
	local a = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[1]);
	local l = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[2]);
	local o = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[3]);
	local J = a .. ("," .. (l .. ("," .. o)));
	t.Text = "<font color=\"rgb(" .. (J .. ")\">Long Béo Ú Hub </font> : Blox Fruits");
	c = Instance.new("ImageLabel");
	c.Name = "MainContainer";
	c.Parent = P;
	c.BackgroundColor3 = G.UIColor["Background Main Color"];
	c.Size = UDim2.new(1, 0, 1, 0);
	c.Transparency = .8;
	local W = Instance.new("UIStroke", c);
	W.Thickness = 2;
	W.Color = Color3.fromRGB(255, 255, 255);
	W.Transparency = .8;
	G.ReadyForGuiLoaded = true;
	local v = Instance.new("ImageLabel", c);
	v.Image = "rbxassetid://131407996827614";
	v.BackgroundTransparency = 1;
	v.ImageTransparency = .8;
	v.Position = UDim2.new(0, -50, 0, -80);
	v.Size = UDim2.new(1, 100, 1, 157);
	v.ZIndex = 0;
	w.CornerRadius = UDim.new(0, 4);
	w.Name = "MainCorner";
	w.Parent = c;
	j.Name = "Concacontainer";
	j.Parent = c;
	j.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	j.BackgroundTransparency = 1.0;
	j.ClipsDescendants = true;
	j.Position = UDim2.new(0, 0, 0, 30);
	j.Size = UDim2.new(1, 0, 1, -30);
	n.Name = "Concacmain";
	n.Parent = j;
	n.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	n.BackgroundTransparency = 1.0;
	n.Selectable = true;
	n.Size = UDim2.new(1, 0, 1, 0);
	A.Name = "TopMain";
	A.Parent = c;
	A.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	A.BackgroundTransparency = 1.0;
	A.Size = UDim2.new(1, 0, 0, 25);
	f.Name = "Ruafimg";
	f.Parent = A;
	f.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	f.BackgroundTransparency = 1.0;
	f.Position = UDim2.new(0, 5, 0, G.T1 and 5 or 0);
	f.Size = UDim2.new(0, G.T1 and 30 or 25, 0, G.T1 and 15 or 25);
	f.Image = "rbxassetid://AnhDau";
	t.Name = "TextLabelMain";
	t.Parent = A;
	t.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
	t.BackgroundTransparency = 1.0;
	t.Position = UDim2.new(0, G.T1 and 40 or 35, 0, 0);
	t.Size = UDim2.new(1, G.T1 and -40 or -35, 1, 0);
	t.Font = Enum.Font.GothamBold;
	t.RichText = true;
	t.TextSize = 16.0;
	t.TextWrapped = true;
	t.TextXAlignment = Enum.TextXAlignment.Center;
	t.TextColor3 = G.UIColor["GUI Text Color"];
	local k = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[1]);
	local z = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[2]);
	local x = tostring((r.Getcolor(G.UIColor["Title Text Color"]))[3]);
	local d = k .. ("," .. (z .. ("," .. x)));
	t.Text = "<font color=\"rgb(" .. (d .. ")\">Long Béo Ú Hub </font> : Blox Fruits");
	i.Name = "Background1";
	i.Parent = n;
	i.Position = UDim2.new(0, 5, 0, 0);
	i.Size = UDim2.new(0, 160, 0, 325);
	i.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
	i.BackgroundColor3 = G.UIColor["Background 1 Color"];
	local O = Instance.new("UIGradient", i);
	O.Transparency = NumberSequence.new({ NumberSequenceKeypoint.new(.0, .1), NumberSequenceKeypoint.new(1.0, .1) });
	O.Name = "thua";
	O.Color = ColorSequence.new({ ColorSequenceKeypoint.new(.0, Color3.fromRGB(22, 22, 22)), ColorSequenceKeypoint.new(1.0, Color3.fromRGB(44, 44, 44)) });
	D.CornerRadius = UDim.new(0, 4);
	D.Parent = i;
	p.Name = "ControlList";
	p.Parent = i;
	p.Active = true;
	p.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
	p.BackgroundTransparency = 1.0;
	p.BorderColor3 = Color3.fromRGB(27, 42, 53);
	p.BorderSizePixel = 0;
	p.Position = UDim2.new(0, 0, 0, 30);
	p.Size = UDim2.new(1, -5, 1, -30);
	p.BottomImage = "rbxasset://textures/ui/Scroll/scroll-middle.png";
	p.CanvasSize = UDim2.new(0, 0, 0, 0);
	p.ScrollBarThickness = 5;
	p.TopImage = "rbxasset://textures/ui/Scroll/scroll-middle.png";
	S.Parent = p;
	S.SortOrder = Enum.SortOrder.LayoutOrder;
	S.Padding = UDim.new(0, 5);
	U.Name = "GUITextColor";
	U.Parent = i;
	U.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
	U.BackgroundTransparency = 1.0;
	U.Position = UDim2.new(0, 5, 0, 0);
	U.Size = UDim2.new(1, 0, 0, 25);
	U.Font = Enum.Font.GothamBold;
	U.Text = X;
	U.TextSize = 14.0;
	U.TextXAlignment = Enum.TextXAlignment.Center;
	U.TextColor3 = G.UIColor["GUI Text Color"];
	b.Name = "MainPage";
	b.Parent = n;
	b.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
	b.BackgroundTransparency = 1.0;
	b.ClipsDescendants = true;
	b.Position = UDim2.new(0, 170, 0, 0);
	b.Size = UDim2.new(0, 453, 0, 325);
	F.Name = "UIPage";
	F.Parent = b;
	F.FillDirection = Enum.FillDirection.Vertical;
	F.SortOrder = Enum.SortOrder.LayoutOrder;
	F.EasingDirection = Enum.EasingDirection.InOut;
	F.EasingStyle = Enum.EasingStyle.Quart;
	F.Padding = UDim.new(0, 10);
	F.TweenTime = G.UIColor["Tween Animation 1 Speed"];
	(S:GetPropertyChangedSignal("AbsoluteContentSize")):Connect(function()
		p.CanvasSize = UDim2.new(0, 0, 0, S.AbsoluteContentSize.Y + 5);
	end);
	local E = Instance.new("Frame");
	local y = Instance.new("UICorner");
	local g = Instance.new("Frame");
	local N = Instance.new("ImageLabel");
	local Q = Instance.new("TextButton");
	local B = Instance.new("TextBox");
	E.Name = "Page Search";
	E.Parent = i;
	E.AnchorPoint = Vector2.new(1, 0);
	E.BackgroundColor3 = Color3.fromRGB(37, 36, 44);
	E.Position = UDim2.new(1, -5, 0, 5);
	E.Size = UDim2.new(0, 20, 0, 20);
	E.ClipsDescendants = true;
	y.CornerRadius = UDim.new(0, 2);
	y.Name = "PageSearchCorner";
	y.Parent = E;
	g.Name = "SearchFrame";
	g.Parent = E;
	g.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	g.BackgroundTransparency = 1.0;
	g.Size = UDim2.new(0, 20, 0, 20);
	N.Name = "SearchIcon";
	N.Parent = g;
	N.AnchorPoint = Vector2.new(.5, .5);
	N.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	N.BackgroundTransparency = 1.0;
	N.Position = UDim2.new(.5, 0, .5, 0);
	N.Size = UDim2.new(0, 16, 0, 16);
	N.Image = "rbxassetid://8154282545";
	N.ImageColor3 = G.UIColor["Search Icon Color"];
	Q.Name = "Search Button";
	Q.Parent = g;
	Q.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	Q.BackgroundTransparency = 1.0;
	Q.Size = UDim2.new(1, 0, 1, 0);
	Q.Font = Enum.Font.SourceSans;
	Q.Text = "";
	Q.TextColor3 = Color3.fromRGB(0, 0, 0);
	Q.TextSize = 14.0;
	B.Name = "Search Box";
	B.Parent = E;
	B.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
	B.BackgroundTransparency = 1.0;
	B.Position = UDim2.new(0, 30, 0, 0);
	B.Size = UDim2.new(1, -30, 1, 0);
	B.Font = Enum.Font.GothamBold;
	B.Text = "";
	B.TextSize = 14.0;
	B.TextXAlignment = Enum.TextXAlignment.Left;
	B.PlaceholderText = "Search section or function";
	B.PlaceholderColor3 = G.UIColor["Placeholder Text Color"];
	B.TextColor3 = G.UIColor["Text Color"];
	local Z = true;
	Q.MouseEnter:Connect(function()
		(C:Create(N, TweenInfo.new(G.UIColor["Tween Animation 3 Speed"]), { ImageColor3 = G.UIColor["Search Icon Highlight Color"] })):Play();
	end);
	Q.MouseLeave:Connect(function()
		(C:Create(N, TweenInfo.new(G.UIColor["Tween Animation 3 Speed"]), { ImageColor3 = G.UIColor["Search Icon Color"] })):Play();
	end);
	Q.MouseButton1Click:Connect(function()
		Z = not Z;
		local M = Z and UDim2.new(0, 150, 0, 20) or UDim2.new(0, 20, 0, 20);
		(game.TweenService:Create(E, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Size = M })):Play();
	end);
	local q = Z and UDim2.new(0, 150, 0, 20) or UDim2.new(0, 20, 0, 20);
	(game.TweenService:Create(E, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Size = q })):Play();
	local h = {};
	local V = -1;
	local H = -1;
	local e = 1;
	function h.CreatePage(M)
		local X = tostring(M.Page_Name);
		local I = tostring(M.Page_Title);
		H = H + 1;
		V = V + 1;
		local Y = Instance.new("Frame");
		local P = Instance.new("Frame");
		local s = Instance.new("UICorner");
		local w = Instance.new("Frame");
		local r = Instance.new("Frame");
		local A = Instance.new("UICorner");
		local m = Instance.new("Frame");
		local f = Instance.new("TextLabel");
		local t = Instance.new("TextButton");
		Y.Name = X .. "_Control";
		Y.Parent = p;
		Y.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		Y.BackgroundTransparency = 1.0;
		Y.Size = UDim2.new(1, -10, 0, 25);
		Y.LayoutOrder = V;
		P.Parent = Y;
		P.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		P.BackgroundTransparency = 1.0;
		P.Position = UDim2.new(0, 5, 0, 0);
		P.Size = UDim2.new(1, -5, 1, 0);
		s.CornerRadius = UDim.new(0, 4);
		s.Name = "TabNameCorner";
		s.Parent = P;
		w.Name = "Line";
		w.Parent = P;
		w.AnchorPoint = Vector2.new(0, .5);
		w.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		w.BackgroundTransparency = 1.0;
		w.Position = UDim2.new(0, 0, .5, 0);
		w.Size = UDim2.new(0, 14, 1, 0);
		r.Name = "PageInLine";
		r.Parent = w;
		r.AnchorPoint = Vector2.new(.5, .5);
		r.BorderSizePixel = 0;
		r.Position = UDim2.new(.5, 0, .5, 0);
		r.Size = UDim2.new(1, -10, 1, -10);
		r.BackgroundColor3 = G.UIColor["Page Selected Color"];
		r.BackgroundTransparency = 1.0;
		A.Name = "LineCorner";
		A.Parent = r;
		m.Name = "TabTitleContainer";
		m.Parent = P;
		m.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		m.BackgroundTransparency = 1.0;
		m.Position = UDim2.new(0, 15, 0, 0);
		m.Size = UDim2.new(1, -15, 1, 0);
		f.Name = "GUITextColor";
		f.Parent = m;
		f.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		f.BackgroundTransparency = 1.0;
		f.Size = UDim2.new(1, 0, 1, 0);
		f.Font = Enum.Font.GothamBold;
		f.Text = X;
		f.TextColor3 = Color3.fromRGB(230, 230, 230);
		f.TextSize = 14.0;
		f.TextXAlignment = Enum.TextXAlignment.Left;
		f.TextColor3 = G.UIColor["GUI Text Color"];
		t.Name = "PageButton";
		t.Parent = Y;
		t.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		t.BackgroundTransparency = 1.0;
		t.Size = UDim2.new(1, 0, 1, 0);
		t.Font = Enum.Font.SourceSans;
		t.Text = "";
		t.TextColor3 = Color3.fromRGB(0, 0, 0);
		t.TextSize = 14.0;
		local i = Instance.new("Frame");
		local D = Instance.new("UICorner");
		local S = Instance.new("TextLabel");
		local U = Instance.new("ScrollingFrame");
		local j = Instance.new("UIListLayout");
		local n = e;
		e = e + 1;
		i.Name = "Page" .. n;
		i.Parent = b;
		i.BackgroundColor3 = G.UIColor["Background 1 Color"];
		i.Position = UDim2.new(0, 190, 0, 30);
		i.Size = UDim2.new(0, 453, 0, 325);
		i.LayoutOrder = H;
		i.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
		D.CornerRadius = UDim.new(0, 4);
		D.Parent = i;
		S.Name = "GUITextColor";
		S.Parent = i;
		S.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		S.BackgroundTransparency = 1.0;
		S.Position = UDim2.new(0, 5, 0, 0);
		S.Size = UDim2.new(1, 0, 0, 25);
		S.Font = Enum.Font.GothamBold;
		S.Text = I;
		S.TextSize = 16.0;
		S.TextXAlignment = Enum.TextXAlignment.Left;
		S.TextColor3 = G.UIColor["GUI Text Color"];
		U.Name = "PageList";
		U.Parent = i;
		U.Active = true;
		U.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
		U.BackgroundTransparency = 1.0;
		U.BorderColor3 = Color3.fromRGB(27, 42, 53);
		U.BorderSizePixel = 0;
		U.Position = UDim2.new(0, 5, 0, 30);
		U.Size = UDim2.new(1, -10, 1, -30);
		U.BottomImage = "rbxasset://textures/ui/Scroll/scroll-middle.png";
		U.ScrollBarThickness = 5;
		U.TopImage = "rbxasset://textures/ui/Scroll/scroll-middle.png";
		U.ScrollingEnabled = true;
		U.VerticalScrollBarInset = Enum.ScrollBarInset.Always;
		j.Name = "Pagelistlayout";
		j.Parent = U;
		j.SortOrder = Enum.SortOrder.LayoutOrder;
		j.Padding = UDim.new(0, 5);
		(j:GetPropertyChangedSignal("AbsoluteContentSize")):Connect(function()
			U.CanvasSize = UDim2.new(0, 0, 0, j.AbsoluteContentSize.Y);
		end);
		local c = Instance.new("Frame");
		local a = Instance.new("UICorner");
		local l = Instance.new("Frame");
		local o = Instance.new("ImageLabel");
		local J = Instance.new("TextButton");
		local W = Instance.new("TextBox");
		c.Name = "Page Search";
		c.Parent = i;
		c.AnchorPoint = Vector2.new(1, 0);
		c.BackgroundColor3 = Color3.fromRGB(37, 36, 44);
		c.Position = UDim2.new(1, -5, 0, 5);
		c.Size = UDim2.new(0, 20, 0, 20);
		c.ClipsDescendants = true;
		a.CornerRadius = UDim.new(0, 2);
		a.Name = "PageSearchCorner";
		a.Parent = c;
		l.Name = "SearchFrame";
		l.Parent = c;
		l.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
		l.BackgroundTransparency = 1.0;
		l.Size = UDim2.new(0, 20, 0, 20);
		o.Name = "SearchIcon";
		o.Parent = l;
		o.AnchorPoint = Vector2.new(.5, .5);
		o.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
		o.BackgroundTransparency = 1.0;
		o.Position = UDim2.new(.5, 0, .5, 0);
		o.Size = UDim2.new(0, 16, 0, 16);
		o.Image = "rbxassetid://8154282545";
		o.ImageColor3 = G.UIColor["Search Icon Color"];
		J.Name = "Search Button";
		J.Parent = l;
		J.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
		J.BackgroundTransparency = 1.0;
		J.Size = UDim2.new(1, 0, 1, 0);
		J.Font = Enum.Font.SourceSans;
		J.Text = "";
		J.TextColor3 = Color3.fromRGB(0, 0, 0);
		J.TextSize = 14.0;
		W.Name = "Search Box";
		W.Parent = c;
		W.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
		W.BackgroundTransparency = 1.0;
		W.Position = UDim2.new(0, 30, 0, 0);
		W.Size = UDim2.new(1, -30, 1, 0);
		W.Font = Enum.Font.GothamBold;
		W.Text = "";
		W.TextSize = 14.0;
		W.TextXAlignment = Enum.TextXAlignment.Left;
		W.PlaceholderText = "Search section or function";
		W.PlaceholderColor3 = G.UIColor["Placeholder Text Color"];
		W.TextColor3 = G.UIColor["Text Color"];
		local v = false;
		J.MouseEnter:Connect(function()
			(C:Create(o, TweenInfo.new(G.UIColor["Tween Animation 3 Speed"]), { ImageColor3 = G.UIColor["Search Icon Highlight Color"] })):Play();
		end);
		J.MouseLeave:Connect(function()
			(C:Create(o, TweenInfo.new(G.UIColor["Tween Animation 3 Speed"]), { ImageColor3 = G.UIColor["Search Icon Color"] })):Play();
		end);
		J.MouseButton1Click:Connect(function()
			v = not v;
			local M = v and UDim2.new(0, 150, 0, 20) or UDim2.new(0, 20, 0, 20);
			(game.TweenService:Create(c, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Size = M })):Play();
		end);
		(W:GetPropertyChangedSignal("Text")):Connect(function()
			local M = W.Text;
			if M == "" then
				for G, M in pairs(p:GetChildren()) do
					if not M:IsA("UIListLayout") then
						M.Visible = true;
					end;
				end;
				for G, M in pairs(b:GetChildren()) do
					if not M:IsA("UIPageLayout") and not M:IsA("UICorner") then
						M.Visible = true;
					end;
				end;
				for G, M in pairs(u) do
					G.Visible = true;
					for G, M in pairs(M) do
						M.Visible = true;
					end;
				end;
			else
				for G, M in pairs(u) do
					G.Visible = false;
					for G, M in pairs(M) do
						M.Visible = false;
					end;
				end;
				for G, M in pairs(p:GetChildren()) do
					if not M:IsA("UIListLayout") then
						M.Visible = false;
					end;
				end;
				for G, M in pairs(b:GetChildren()) do
					if not M:IsA("UIPageLayout") and not M:IsA("UICorner") then
						M.Visible = false;
					end;
				end;
				for X, I in pairs(G.listfunction) do
					for I, Y in pairs(I) do
						if string.find(Y.Name:lower(), M:lower()) then
							if Y.Call then
								Y.Call();
							end;
							local M = G.listtab[X];
							if M then
								M[1].Visible = true;
								M[2].Visible = true;
								M[3].Visible = true;
								local X = G.UIColor["Tween Animation 1 Speed"];
								F.TweenTime = 0;
								F:JumpTo(M[2]);
								task.wait();
								F.TweenTime = X;
							end;
						end;
					end;
				end;
			end;
		end);
		function visiblealloff()
			for G, M in pairs(p:GetChildren()) do
				if not M:IsA("UIListLayout") then
					M.Visible = false;
				end;
			end;
			for G, M in pairs(b:GetChildren()) do
				if not M:IsA("UIPageLayout") and not M:IsA("UICorner") then
					M.Visible = false;
				end;
			end;
		end;
		O = visiblealloff;
		for G, M in pairs(p:GetChildren()) do
			if not M:IsA("UIListLayout") then
				if G == 2 then
					M.Frame.Line.PageInLine.BackgroundTransparency = 0;
				end;
			end;
		end;
		t.MouseButton1Click:Connect(function()
			if tostring(F.CurrentPage) == i.Name then
				return;
			end;
			for G, M in pairs(b:GetChildren()) do
				if not M:IsA("UIPageLayout") and not M:IsA("UICorner") then
					M.Visible = false;
				end;
			end;
			i.Visible = true;
			F:JumpTo(i);
			for M, I in next, p:GetChildren() do
				if not I:IsA("UIListLayout") then
					if I.Name == X .. "_Control" then
						(C:Create(I.Frame.Line.PageInLine, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = 0 })):Play();
					else
						(C:Create(I.Frame.Line.PageInLine, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = 1 })):Play();
					end;
				end;
			end;
		end);
		local k = {};
		function k.CreateSection(M, X, I, P)
			local s = X or false;
			local w = Instance.new("Frame");
			local r = Instance.new("UICorner");
			local A = Instance.new("Frame");
			local m = Instance.new("TextLabel");
			local f = Instance.new("Frame");
			local t = Instance.new("UIGradient");
			local D = Instance.new("UIListLayout");
			G.listtab[w] = { [1] = Y, [2] = i, [3] = w };
			G.listfunction[w] = {};
			w.Name = M .. "_Dot";
			w.Parent = U;
			w.Size = UDim2.new(1, -5, 0, 30);
			w.BackgroundColor3 = G.UIColor["Background 3 Color"];
			w.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
			w.ClipsDescendants = true;
			u[w] = {};
			r.CornerRadius = UDim.new(0, 4);
			r.Parent = w;
			local p = Instance.new("UIGradient", w);
			p.Name = "thua2";
			p.Color = ColorSequence.new({ ColorSequenceKeypoint.new(.0, Color3.fromRGB(22, 22, 22)), ColorSequenceKeypoint.new(1.0, Color3.fromRGB(44, 44, 44)) });
			A.Name = "Topsec";
			A.Parent = w;
			A.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
			A.BackgroundTransparency = 1.0;
			A.Size = UDim2.new(0, 415, 0, 30);
			m.Name = "Sectiontitle";
			m.Parent = A;
			m.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
			m.BackgroundTransparency = 1.0;
			m.Size = UDim2.new(1, 0, 1, 0);
			m.Font = Enum.Font.GothamBold;
			m.Text = M;
			m.TextSize = 14.0;
			m.TextColor3 = P and P or G.UIColor["Section Text Color"];
			f.Name = "Linesec";
			f.Parent = A;
			f.AnchorPoint = Vector2.new(.5, 1);
			f.BorderSizePixel = 0;
			f.Position = UDim2.new(.5, 0, 1, -2);
			f.Size = UDim2.new(1, -10, 0, 2);
			f.BackgroundColor3 = P and P or G.UIColor["Section Underline Color"];
			local S;
			local b = false;
			if s then
				local M = Instance.new("Frame");
				local X = Instance.new("UICorner");
				local I = Instance.new("ImageButton");
				local Y = Instance.new("ImageButton");
				local u = Instance.new("TextButton");
				u.Name = "VisibilityButton";
				u.Parent = A;
				u.AnchorPoint = Vector2.new(1, .5);
				u.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
				u.BackgroundTransparency = 1.0;
				u.BorderColor3 = Color3.fromRGB(0, 0, 0);
				u.BorderSizePixel = 0;
				u.Font = Enum.Font.SourceSans;
				u.Text = "";
				u.TextColor3 = Color3.fromRGB(0, 0, 0);
				u.TextSize = 14.0;
				u.ZIndex = 2;
				u.Position = UDim2.new(1, -5, .5, 0);
				u.Size = UDim2.new(0, 20, 0, 20);
				M.Name = "VisibilitySectionFrame";
				M.Parent = A;
				M.AnchorPoint = Vector2.new(1, .5);
				M.BackgroundColor3 = Color3.fromRGB(30, 30, 30);
				M.BorderColor3 = Color3.fromRGB(0, 0, 0);
				M.BorderSizePixel = 0;
				M.Position = UDim2.new(1, -5, .5, 0);
				M.Size = UDim2.new(0, 20, 0, 20);
				X.CornerRadius = UDim.new(0, 4);
				X.Name = "VisibilitySectionFrameCorner";
				X.Parent = M;
				I.Name = "visibility";
				I.Parent = M;
				I.AnchorPoint = Vector2.new(.5, .5);
				I.BackgroundTransparency = 1.0;
				I.LayoutOrder = 4;
				I.Position = UDim2.new(.5, 0, .5, 0);
				I.Size = UDim2.new(1, -4, 1, -4);
				I.ZIndex = 2;
				I.Image = "rbxassetid://3926307971";
				I.ImageRectOffset = Vector2.new(84, 44);
				I.ImageRectSize = Vector2.new(36, 36);
				I.ImageTransparency = 1;
				Y.Name = "visibility_off";
				Y.Parent = M;
				Y.AnchorPoint = Vector2.new(.5, .5);
				Y.BackgroundTransparency = 1.0;
				Y.LayoutOrder = 4;
				Y.Position = UDim2.new(.5, 0, .5, 0);
				Y.Size = UDim2.new(1, -4, 1, -4);
				Y.ZIndex = 2;
				Y.Image = "rbxassetid://3926307971";
				Y.ImageRectOffset = Vector2.new(564, 44);
				Y.ImageRectSize = Vector2.new(36, 36);
				Y.ImageTransparency = 0;
				u.MouseButton1Down:Connect(function()
					b = not b;
					(C:Create(I, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"] / 2), { ImageTransparency = b and 0 or 1 })):Play();
					wait(G.UIColor["Tween Animation 1 Speed"] / 4);
					(C:Create(Y, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"] / 2), { ImageTransparency = b and 1 or 0 })):Play();
					(C:Create(w, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { Size = UDim2.new(1, -5, 0, b and S or 30) })):Play();
				end);
			end;
			if I then
				local G = Instance.new("Frame");
				G.Name = "SectionGap";
				G.Parent = U;
				G.Size = UDim2.new(1, -5, 0, 30);
				G.ClipsDescendants = true;
				G.Transparency = 1;
			end;
			t.Transparency = NumberSequence.new({
					NumberSequenceKeypoint.new(.0, 1.0),
					NumberSequenceKeypoint.new(.5, .0),
					NumberSequenceKeypoint.new(.51, .02),
					NumberSequenceKeypoint.new(1.0, 1.0),
				});
			t.Parent = f;
			D.Name = "SectionList";
			D.Parent = w;
			D.SortOrder = Enum.SortOrder.LayoutOrder;
			D.Padding = UDim.new(0, 5);
			local F = -1;
			(D:GetPropertyChangedSignal("AbsoluteContentSize")):Connect(function()
				local M = D.AbsoluteContentSize.Y + 5;
				if M == F then
					return;
				end;
				F = M;
				if not s then
					w.Size = UDim2.new(1, -5, 0, M);
				end;
				S = M;
				if b then
					(C:Create(w, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { Size = UDim2.new(1, -5, 0, S) })):Play();
				end;
			end);
			local j = {};
			function j.CreateToggle(M, X)
				local I = tostring(M.Title or "");
				local Y = M.Desc;
				local P = M.Default;
				if P == nil then
					P = false;
				end;
				local s = X or function()
 
					end;
				local r = Instance.new("Frame");
				local C = Instance.new("Frame");
				local A = Instance.new("ImageLabel");
				local R = Instance.new("ImageLabel");
				local m = Instance.new("TextLabel");
				local f = Instance.new("TextLabel");
				local t = Instance.new("Frame");
				local i = Instance.new("UICorner");
				local D = Instance.new("TextButton");
				local p = Instance.new("UIListLayout");
				r.Name = "ToggleFrame";
				r.Parent = w;
				r.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				r.BackgroundTransparency = 1.0;
				r.Position = UDim2.new(0, 0, .300000012, 0);
				r.Size = UDim2.new(1, 0, 0, 0);
				r.AutomaticSize = Enum.AutomaticSize.Y;
				C.Name = "TogFrame1";
				C.Parent = r;
				C.AnchorPoint = Vector2.new(.5, .5);
				C.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				C.BackgroundTransparency = 1.0;
				C.Position = UDim2.new(.5, 0, .5, 0);
				C.Size = UDim2.new(1, -10, 0, 0);
				C.AutomaticSize = Enum.AutomaticSize.Y;
				A.Name = "checkbox";
				A.Parent = C;
				A.AnchorPoint = Vector2.new(1, .5);
				A.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				A.BackgroundTransparency = 1.0;
				A.Position = UDim2.new(1, -5, .5, 3);
				A.Size = UDim2.new(0, 25, 0, 25);
				A.Image = "rbxassetid://4552505888";
				A.ImageColor3 = G.UIColor["Toggle Border Color"];
				R.Name = "check";
				R.Parent = A;
				R.AnchorPoint = Vector2.new(.5, .5);
				R.BackgroundColor3 = Color3.fromRGB(200, 0, 255);
				R.BackgroundTransparency = 0;
				R.Position = UDim2.new(.5, 0, .5, 0);
				R.Size = UDim2.new(0, 0, 0, 0);
				R.Image = "";
				R.ImageColor3 = G.UIColor["Toggle Checked Color"];
				local S = 5;
				if Y then
					S = 0;
					m.Name = "ToggleDesc";
					m.Parent = C;
					m.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
					m.BackgroundTransparency = 1.0;
					m.Position = UDim2.new(0, 15, 0, 20);
					m.Size = UDim2.new(1, -50, 0, 0);
					m.Font = Enum.Font.GothamBlack;
					m.Text = Y;
					m.TextSize = 13.0;
					m.TextWrapped = true;
					m.TextXAlignment = Enum.TextXAlignment.Left;
					m.RichText = true;
					m.AutomaticSize = Enum.AutomaticSize.Y;
					m.TextColor3 = G.UIColor["Toggle Desc Color"];
				else
					m.Text = "";
				end;
				f.Name = "TextColor";
				f.Parent = C;
				f.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				f.BackgroundTransparency = 1.0;
				f.Position = UDim2.new(0, 10, 0, S);
				f.Size = UDim2.new(1, -10, 0, 20);
				f.Font = Enum.Font.GothamBlack;
				f.Text = I;
				f.TextSize = 14.0;
				f.TextXAlignment = Enum.TextXAlignment.Left;
				f.TextYAlignment = Enum.TextYAlignment.Center;
				f.RichText = true;
				f.AutomaticSize = Enum.AutomaticSize.Y;
				f.TextColor3 = G.UIColor["Text Color"];
				t.Name = "Background1";
				t.Parent = C;
				t.Size = UDim2.new(1, 0, 1, 6);
				t.ZIndex = 0;
				t.BackgroundColor3 = G.UIColor["Background 1 Color"];
				t.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
				i.CornerRadius = UDim.new(0, 4);
				i.Name = "ToggleCorner";
				i.Parent = t;
				D.Name = "ToggleButton";
				D.Parent = C;
				D.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				D.BackgroundTransparency = 1.0;
				D.AnchorPoint = Vector2.new(1, .5);
				D.Size = UDim2.new(0, 25, 0, 25);
				D.Position = UDim2.new(1, -5, .5, 3);
				D.Font = Enum.Font.SourceSans;
				D.Text = "";
				D.TextColor3 = Color3.fromRGB(0, 0, 0);
				D.TextSize = 14.0;
				p.Name = "ToggleList";
				p.Parent = r;
				p.HorizontalAlignment = Enum.HorizontalAlignment.Center;
				p.SortOrder = Enum.SortOrder.LayoutOrder;
				p.VerticalAlignment = Enum.VerticalAlignment.Center;
				p.Padding = UDim.new(0, 5);
				local U = Instance.new("UICorner", R);
				U.CornerRadius = UDim.new(0, 2);
				local function b(M)
					local X = M and UDim2.new(1, -12, 1, -12) or UDim2.new(0, 0, 0, 0);
					local I = UDim2.new(.5, 0, .5, 0);
					local Y = Vector2.new(.5, .5);
					(game.TweenService:Create(R, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { Size = X, Position = I, AnchorPoint = Y })):Play();
					s(M);
				end;
				if s then
					b(P);
				end;
				local function F()
					P = not P;
					b(P);
				end;
				D.MouseButton1Down:Connect(function()
					F();
				end);
				local j = {};
				function j.SetStage(G)
					if G ~= P then
						F();
					end;
				end;
				function visibleon()
					r.Visible = true;
				end;
				table.insert(G.listfunction[w], { Type = "Toggle", Name = I, Call = visibleon });
				table.insert(u[w], r);
				return j;
			end;
			function j.CreateButton(M, X)
				local I = M.Title;
				local Y = X or function()
 
					end;
				local P = Instance.new("Frame", w);
				P.LayoutOrder = 0;
				P.BorderMode = Enum.BorderMode.Outline;
				P.Selectable = false;
				P.AnchorPoint = Vector2.new(0, 0);
				P.AutomaticSize = Enum.AutomaticSize.None;
				P.Size = UDim2.new(1, 0, 0, 40);
				P.Draggable = false;
				P.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				P.Style = Enum.FrameStyle.Custom;
				P.Transparency = 1;
				P.BackgroundTransparency = 1;
				P.SelectionOrder = 0;
				P.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				P.BackgroundColor3 = Color3.new(.63921570777893, .63529413938522, .64705884456635);
				local s = Instance.new("Frame", P);
				s.LayoutOrder = 0;
				s.BorderMode = Enum.BorderMode.Outline;
				s.Selectable = false;
				s.AnchorPoint = Vector2.new(.5, .5);
				s.AutomaticSize = Enum.AutomaticSize.None;
				s.Size = UDim2.new(1, -10, 1, 0);
				s.Draggable = false;
				s.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				s.Style = Enum.FrameStyle.Custom;
				s.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				s.Transparency = G.UIColor["Background 1 Transparency"];
				s.BackgroundTransparency = .25;
				s.Position = UDim2.new(.5, 0, .5, 0);
				s.SelectionOrder = 0;
				s.BackgroundColor3 = G.UIColor["Background 1 Color"];
				local r = Instance.new("UICorner", s);
				r.CornerRadius = UDim.new(0, 10);
				local C = Instance.new("Frame", s);
				C.LayoutOrder = 0;
				C.BorderMode = Enum.BorderMode.Outline;
				C.Selectable = false;
				C.AnchorPoint = Vector2.new(0, 0);
				C.ZIndex = 2;
				C.AutomaticSize = Enum.AutomaticSize.None;
				C.Draggable = false;
				C.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				C.Style = Enum.FrameStyle.Custom;
				C.Transparency = 1;
				C.BackgroundTransparency = 1;
				C.SelectionOrder = 0;
				C.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				C.BackgroundColor3 = Color3.new(.18823529779911, .18823529779911, .21960784494877);
				local A = Instance.new("UICorner", C);
				A.CornerRadius = UDim.new(0, 10);
				local R = Instance.new("TextLabel", s);
				R.LineHeight = 1;
				R.Active = false;
				R.TextStrokeTransparency = .85000002384186;
				R.TextTruncate = Enum.TextTruncate.None;
				R.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				R.ZIndex = 1;
				R.BorderSizePixel = 1;
				R.Draggable = false;
				R.RichText = false;
				R.SelectionOrder = 0;
				R.BackgroundColor3 = Color3.new(.63921570777893, .63529413938522, .64705884456635);
				R.BorderMode = Enum.BorderMode.Outline;
				R.TextStrokeColor3 = Color3.new(0, 0, 0);
				R.AnchorPoint = Vector2.new(0, 0);
				R.AutomaticSize = Enum.AutomaticSize.None;
				R.Size = UDim2.new(1, -110, 1, 0);
				R.TextColor3 = Color3.new(.92156863212585, .92156863212585, .90196079015732);
				R.ClipsDescendants = false;
				R.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				R.Text = I;
				R.TextXAlignment = Enum.TextXAlignment.Left;
				R.LayoutOrder = 0;
				R.Rotation = 0;
				R.Font = Enum.Font.GothamBold;
				R.BackgroundTransparency = 1;
				R.Position = UDim2.new(0, 12, 0, 0);
				R.Selectable = false;
				R.MaxVisibleGraphemes = -1;
				R.Visible = true;
				R.TextSize = 14;
				local m = Instance.new("Frame", s);
				m.LayoutOrder = 0;
				m.BorderMode = Enum.BorderMode.Outline;
				m.Selectable = false;
				m.AnchorPoint = Vector2.new(1, .5);
				m.AutomaticSize = Enum.AutomaticSize.None;
				m.Size = UDim2.new(0, 94, 0, 30);
				m.Draggable = false;
				m.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				m.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				m.Transparency = 0;
				m.Style = Enum.FrameStyle.Custom;
				m.Position = UDim2.new(1, -8, .5, 0);
				m.SelectionOrder = 0;
				m.BackgroundColor3 = Color3.new(.63921570777893, .63529413938522, .64705884456635);
				local f = Instance.new("UICorner", m);
				f.CornerRadius = UDim.new(0, 12);
				local t = Instance.new("UIGradient", m);
				t.Enabled = true;
				t.Transparency = NumberSequence.new({ NumberSequenceKeypoint.new(0, 0, 0), NumberSequenceKeypoint.new(1, 0, 0) });
				t.Color = ColorSequence.new({ ColorSequenceKeypoint.new(.0, Color3.fromRGB(201, 0, 255)), ColorSequenceKeypoint.new(1.0, Color3.fromRGB(201, 0, 255)) });
				t.Offset = Vector2.new(0, 0);
				t.Rotation = 90;
				local i = Instance.new("TextButton", m);
				i.Visible = true;
				i.TextWrapped = false;
				i.LineHeight = 1;
				i.Active = true;
				i.TextStrokeTransparency = 1;
				i.TextTruncate = Enum.TextTruncate.None;
				i.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				i.ZIndex = 1;
				i.BorderSizePixel = 1;
				i.Draggable = false;
				i.RichText = false;
				i.AutoButtonColor = false;
				i.Transparency = 1;
				i.SelectionOrder = 0;
				i.TextYAlignment = Enum.TextYAlignment.Center;
				i.TextScaled = false;
				i.BackgroundColor3 = Color3.new(.63921570777893, .63529413938522, .64705884456635);
				i.BorderMode = Enum.BorderMode.Outline;
				i.Selectable = true;
				i.AnchorPoint = Vector2.new(0, 0);
				i.Style = Enum.ButtonStyle.Custom;
				i.Modal = false;
				i.Selected = false;
				i.AutomaticSize = Enum.AutomaticSize.None;
				i.Size = UDim2.new(1, 0, 1, 0);
				i.TextXAlignment = Enum.TextXAlignment.Center;
				i.TextTransparency = 0;
				i.ClipsDescendants = false;
				i.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				i.Text = "Click";
				i.LayoutOrder = 0;
				i.TextStrokeColor3 = Color3.new(0, 0, 0);
				i.Rotation = 0;
				i.Font = Enum.Font.GothamBold;
				i.BackgroundTransparency = 1;
				i.Position = UDim2.new(0, 0, 0, 0);
				i.TextSize = 13;
				i.MaxVisibleGraphemes = -1;
				i.TextColor3 = Color3.new(.098039217293262, .10980392247438, .14117647707462);
				local D = Instance.new("Frame", m);
				D.LayoutOrder = 0;
				D.BorderMode = Enum.BorderMode.Outline;
				D.Selectable = false;
				D.AnchorPoint = Vector2.new(.5, 0);
				D.ZIndex = 2;
				D.AutomaticSize = Enum.AutomaticSize.None;
				D.Size = UDim2.new(1, -6, 0, 10);
				D.Draggable = false;
				D.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				D.Style = Enum.FrameStyle.Custom;
				D.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				D.Transparency = .85000002384186;
				D.BackgroundTransparency = .85000002384186;
				D.Position = UDim2.new(.5, 0, 0, 2);
				D.SelectionOrder = 0;
				D.BackgroundColor3 = Color3.new(1, 1, 1);
				local p = Instance.new("UICorner", D);
				p.CornerRadius = UDim.new(0, 4);
				local S = Instance.new("ImageLabel", m);
				S.LayoutOrder = 0;
				S.BorderMode = Enum.BorderMode.Outline;
				S.SliceCenter = Rect.new(24, 24, 276, 276);
				S.Active = false;
				S.Selectable = false;
				S.Visible = true;
				S.ImageTransparency = .55000001192093;
				S.ImageColor3 = Color3.new(1, 1, 1);
				S.AnchorPoint = Vector2.new(.5, .5);
				S.Image = "rbxassetid://5028857084";
				S.ImageRectOffset = Vector2.new(0, 0);
				S.ImageRectSize = Vector2.new(0, 0);
				S.ZIndex = 0;
				S.AutomaticSize = Enum.AutomaticSize.None;
				S.Size = UDim2.new(1, 14, 1, 14);
				S.Draggable = false;
				S.ScaleType = Enum.ScaleType.Slice;
				S.BorderColor3 = Color3.new(.10588235408068, .16470588743687, .20784313976765);
				S.SizeConstraint = Enum.SizeConstraint.RelativeXY;
				S.SelectionOrder = 0;
				S.ClipsDescendants = false;
				S.Rotation = 0;
				S.Transparency = 1;
				S.BackgroundTransparency = 1;
				S.Position = UDim2.new(.5, 0, .5, 0);
				S.SliceScale = 1;
				S.BorderSizePixel = 1;
				S.BackgroundColor3 = Color3.new(.63921570777893, .63529413938522, .64705884456635);
				i.MouseButton1Click:Connect(function()
					Y();
				end);
				function visibleon()
					P.Visible = true;
				end;
				table.insert(G.listfunction[w], { Type = "Toggle", Name = I, Call = visibleon });
				table.insert(u[w], P);
			end;
			function j.CreateLabel(M)
				local X = tostring(M.Title);
				local I = Instance.new("Frame");
				local Y = Instance.new("Frame");
				local P = Instance.new("UICorner");
				local s = Instance.new("TextLabel");
				I.Name = "LabelFrame";
				I.Parent = w;
				I.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				I.BackgroundTransparency = 1.0;
				I.Position = UDim2.new(0, 0, 0, 0);
				I.Size = UDim2.new(1, 0, 0, 0);
				I.AutomaticSize = Enum.AutomaticSize.Y;
				Y.Name = "LabelBG";
				Y.Parent = I;
				Y.AnchorPoint = Vector2.new(.5, 0);
				Y.Position = UDim2.new(.5, 0, 0, 0);
				Y.Size = UDim2.new(1, -10, 0, -10);
				Y.BackgroundColor3 = G.UIColor["Background 1 Color"];
				Y.AutomaticSize = Enum.AutomaticSize.Y;
				Y.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
				P.CornerRadius = UDim.new(0, 4);
				P.Name = "LabelCorner";
				P.Parent = Y;
				s.Name = "TextColor";
				s.Parent = Y;
				s.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				s.BackgroundTransparency = 1.0;
				s.Position = UDim2.new(0, 10, 0, 3);
				s.Size = UDim2.new(1, -20, 1, 10);
				s.Font = Enum.Font.GothamBlack;
				s.Text = X;
				s.TextSize = 14.0;
				s.TextXAlignment = Enum.TextXAlignment.Left;
				s.AutomaticSize = Enum.AutomaticSize.Y;
				s.TextWrapped = true;
				s.TextColor3 = G.UIColor["Text Color"];
				s.TextStrokeTransparency = G.UIColor["Text Stroke Transparency"];
				s.RichText = true;
				local r = {};
				function r.SetText(G)
					s.Text = G;
				end;
				function r.SetColor(G)
					s.TextColor3 = G;
				end;
				function visibleon()
					I.Visible = true;
				end;
				table.insert(G.listfunction[w], { Type = "Label", Name = X, Call = visibleon });
				table.insert(u[w], I);
				return r;
			end;
			function j.CreateDropdown(M, X)
				local I = tostring(M.Title);
				local Y = M.List;
				local P = M.Search or false;
				local s = M.Selected or false;
				local r = M.Slider or false;
				local A = M.SliderRelease or false;
				local m = M.Default;
				local f = X or function()
 
					end;
				local t = M.IndexTable;
				local i = M.SortPairs or pairs;
				local D = Instance.new("Frame");
				local p = Instance.new("Frame");
				local S = Instance.new("UICorner");
				local U = Instance.new("Frame");
				local b = Instance.new("UICorner");
				local F = Instance.new("ImageLabel");
				local j = Instance.new("TextButton");
				local n = Instance.new("Frame");
				local c = Instance.new("ScrollingFrame");
				local a = Instance.new("Frame");
				local l = Instance.new("UIListLayout");
				local o = false;
				local J;
				if P then
					J = Instance.new("TextBox");
				else
					J = Instance.new("TextLabel");
				end;
				D.Name = I .. "DropdownFrame";
				D.Parent = w;
				D.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				D.BackgroundTransparency = 1.0;
				D.Position = UDim2.new(0, 0, .473684222, 0);
				D.Size = UDim2.new(1, 0, 0, 25);
				p.Name = "Background1";
				p.Parent = D;
				p.AnchorPoint = Vector2.new(.5, .5);
				p.Position = UDim2.new(.5, 0, .5, 0);
				p.Size = UDim2.new(1, -10, 1, 0);
				p.ClipsDescendants = true;
				p.BackgroundColor3 = Color3.fromRGB(28, 28, 34);
				p.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
				p.BackgroundTransparency = .25;
				S.CornerRadius = UDim.new(0, 4);
				S.Name = "Dropdowncorner";
				S.Parent = p;
				U.Name = "Background2";
				U.Parent = p;
				U.Size = UDim2.new(1, 0, 0, 25);
				U.BackgroundColor3 = Color3.fromRGB(38, 38, 46);
				U.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
				U.BackgroundTransparency = .25;
				b.CornerRadius = UDim.new(0, 4);
				b.Parent = U;
				J.Name = "TextColorPlaceholder";
				J.Parent = U;
				J.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				J.BackgroundTransparency = 1.0;
				J.Position = UDim2.new(0, 10, 0, 0);
				J.Size = UDim2.new(1, -40, 1, 0);
				J.Font = Enum.Font.GothamBlack;
				J.Text = "";
				J.TextSize = 14.0;
				J.TextXAlignment = Enum.TextXAlignment.Left;
				J.ClipsDescendants = true;
				local W = Instance.new("StringValue", J);
				W.Value = "";
				if m and table.find(Y, m) then
					W.Value = m;
				end;
				if not s then
					if P then
						J.PlaceholderColor3 = G.UIColor["Placeholder Text Color"];
						J.PlaceholderText = I .. (": " .. tostring(m or ""));
					else
						J.Text = I .. (": " .. tostring(m or ""));
					end;
				else
					if P then
						J.PlaceholderColor3 = G.UIColor["Placeholder Text Color"];
						J.PlaceholderText = I .. (": " .. tostring(m or ""));
					else
						J.Text = I .. (": " .. tostring(m or ""));
					end;
				end;
				J.TextColor3 = G.UIColor["Text Color"];
				F.Name = "ImgDrop";
				F.Parent = U;
				F.AnchorPoint = Vector2.new(1, .5);
				F.BackgroundTransparency = 1.0;
				F.BorderColor3 = Color3.fromRGB(27, 42, 53);
				F.Position = UDim2.new(1, -6, .5, 0);
				F.Size = UDim2.new(0, 15, 0, 15);
				F.Image = "rbxassetid://6954383209";
				F.ImageColor3 = G.UIColor["Dropdown Icon Color"];
				j.Name = "DropdownButton";
				j.Parent = U;
				j.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				j.BackgroundTransparency = 1.0;
				j.Size = P and UDim2.new(0, 30, 0, 30) or UDim2.new(1, 0, 1, 0);
				j.Position = P and UDim2.new(1, -35, 0, 0) or UDim2.new(0, 0, 0, 0);
				j.Font = Enum.Font.GothamBold;
				j.Text = "";
				j.TextColor3 = Color3.fromRGB(230, 230, 230);
				j.TextSize = 14.0;
				n.Name = "Dropdownlisttt";
				n.Parent = p;
				n.BackgroundTransparency = 1.0;
				n.BorderSizePixel = 0;
				n.Position = UDim2.new(0, 0, 0, 25);
				n.Size = UDim2.new(1, 0, 0, 25);
				n.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				c.Name = "DropdownScroll";
				c.Parent = n;
				c.Active = true;
				c.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				c.BackgroundTransparency = 1.0;
				c.BorderSizePixel = 0;
				c.Size = UDim2.new(1, 0, 1, 0);
				c.BottomImage = "rbxasset://textures/ui/Scroll/scroll-middle.png";
				c.CanvasSize = UDim2.new(0, 0, 0, 0);
				c.ScrollBarThickness = 5;
				c.TopImage = "rbxasset://textures/ui/Scroll/scroll-middle.png";
				c.ScrollingEnabled = true;
				c.VerticalScrollBarInset = Enum.ScrollBarInset.Always;
				a.Name = "ScrollContainer";
				a.Parent = c;
				a.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				a.BackgroundTransparency = 1.0;
				a.Position = UDim2.new(0, 5, 0, 5);
				a.Size = UDim2.new(1, -15, 1, -5);
				l.Name = "ScrollContainerList";
				l.Parent = a;
				l.SortOrder = Enum.SortOrder.LayoutOrder;
				l.Padding = UDim.new(0, 5);
				(l:GetPropertyChangedSignal("AbsoluteContentSize")):Connect(function()
					c.CanvasSize = UDim2.new(0, 0, 0, (10 + l.AbsoluteContentSize.Y) + 5);
				end);
				local v = false;
				local k = {};
				local z = {};
				local function x()
					for G in i(k) do
						k[G] = nil;
					end;
					for G, M in i(a:GetChildren()) do
						if not M:IsA("UIListLayout") and (not M:IsA("UIPadding") and not M:IsA("UIGridLayout")) then
							M.Visible = false;
						end;
					end;
					J.Text = string.lower(J.Text);
				end;
				local function d()
					local G = {};
					for G, M in i(z) do
						if string.find(M, J.Text) then
							table.insert(k, M);
						end;
					end;
					for G, M in i(a:GetChildren()) do
						for G, X in i(k) do
							if X == M.Name then
								M.Visible = true;
							end;
						end;
					end;
				end;
				local function O()
					for G, M in next, a:GetChildren() do
						if M:IsA("Frame") then
							M:Destroy();
						end;
					end;
				end;
				local E = Y;
				local function y(M)
					i = M or i;
					O();
					z = {};
					for G, M in i(E) do
						if s then
							table.insert(z, string.lower(G));
						elseif r then
							table.insert(z, string.lower(M.Title));
						else
							table.insert(z, string.lower(M));
						end;
					end;
					if s then
						for M, X in i(E) do
							local Y = Instance.new("Frame");
							local u = Instance.new("UICorner");
							local s = Instance.new("Frame");
							local w = Instance.new("UICorner");
							local r = Instance.new("TextLabel");
							local A = Instance.new("ImageButton");
							local R = Instance.new("TextButton");
							Y.Name = string.lower(M);
							Y.Parent = a;
							Y.BackgroundColor3 = Color3.fromRGB(60, 60, 60);
							Y.BackgroundTransparency = 1.0;
							Y.BorderColor3 = Color3.fromRGB(27, 42, 53);
							Y.LayoutOrder = 1;
							Y.Position = UDim2.new(0, 0, .208333328, 0);
							Y.Size = UDim2.new(1, 0, 0, 25);
							u.CornerRadius = UDim.new(0, 4);
							u.Name = "SampleItemCorner";
							u.Parent = Y;
							s.Name = "SampleItemBG";
							s.Parent = Y;
							s.AnchorPoint = Vector2.new(.5, .5);
							s.BackgroundColor3 = X and G.UIColor["Dropdown Selected Check Color"] or Color3.fromRGB(255, 255, 255);
							s.BackgroundTransparency = X and .5 or 1;
							s.BorderColor3 = Color3.fromRGB(27, 42, 53);
							s.Position = UDim2.new(.5, 0, .5, 0);
							s.Size = UDim2.new(1, 0, 1, 0);
							w.CornerRadius = UDim.new(0, 4);
							w.Name = "SampleItemBGCorner";
							w.Parent = s;
							r.Name = "SampleItemTitle";
							r.Parent = s;
							r.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
							r.BackgroundTransparency = 1.0;
							r.BorderColor3 = Color3.fromRGB(27, 42, 53);
							r.Position = UDim2.new(0, 10, 0, 0);
							r.Size = UDim2.new(1, -40, 0, 25);
							r.Font = Enum.Font.GothamBlack;
							r.Text = M;
							r.TextColor3 = Color3.fromRGB(255, 255, 255);
							r.TextSize = 14.0;
							r.TextStrokeTransparency = .5;
							r.TextXAlignment = Enum.TextXAlignment.Left;
							A.Name = "SampleItemCheck";
							A.Parent = s;
							A.AnchorPoint = Vector2.new(1, .5);
							A.BackgroundTransparency = 1.0;
							A.Position = UDim2.new(1, 0, .5, 0);
							A.Size = UDim2.new(0, 25, 0, 25);
							A.ZIndex = 2;
							A.Image = "rbxassetid://3926305904";
							A.ImageColor3 = G.UIColor["Dropdown Selected Check Color"];
							A.ImageRectOffset = Vector2.new(312, 4);
							A.ImageRectSize = Vector2.new(24, 24);
							A.ImageTransparency = X and 0 or 1;
							R.Name = "SampleItemButton";
							R.Parent = Y;
							R.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
							R.BackgroundTransparency = 1.0;
							R.BorderColor3 = Color3.fromRGB(0, 0, 0);
							R.BorderSizePixel = 0;
							R.Size = UDim2.new(1, 0, 1, 0);
							R.Font = Enum.Font.SourceSans;
							R.TextColor3 = G.UIColor["Text Color"];
							R.TextSize = 14.0;
							R.TextTransparency = 1.0;
							R.MouseEnter:Connect(function()
								if X then
									return;
								end;
								(C:Create(s, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundColor3 = Color3.fromRGB(255, 255, 255) })):Play();
								(C:Create(s, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = .7 })):Play();
							end);
							R.MouseLeave:Connect(function()
								if X then
									return;
								end;
								(C:Create(s, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundColor3 = Color3.fromRGB(255, 255, 255) })):Play();
								(C:Create(s, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = 1 })):Play();
							end);
							R.MouseButton1Click:Connect(function()
								X = not X;
								(C:Create(A, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { ImageTransparency = X and 0 or 1 })):Play();
								(C:Create(s, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundColor3 = X and G.UIColor["Dropdown Selected Check Color"] or Color3.fromRGB(255, 255, 255) })):Play();
								(C:Create(s, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = X and .5 or 1 })):Play();
								if f then
									f(M, X);
									E[M] = X;
								end;
								if P then
									J.PlaceholderText = I .. ": ";
								else
									J.Text = I .. ": ";
								end;
							end);
						end;
					elseif r then
						for M, X in i(E) do
							local I = tostring(X.Title) or "";
							local Y = tonumber(X.Min) or 0;
							local u = tonumber(X.Max) or 100;
							local P = X.Precise or false;
							local s = tonumber(X.Default) or Y;
							local w = 365;
							local r = Instance.new("Frame");
							local m = Instance.new("UICorner");
							local t = Instance.new("Frame");
							local i = Instance.new("UICorner");
							local D = Instance.new("TextLabel");
							local p = Instance.new("Frame");
							local S = Instance.new("TextButton");
							local U = Instance.new("UICorner");
							local b = Instance.new("Frame");
							local F = Instance.new("UICorner");
							local j = Instance.new("Frame");
							local n = Instance.new("UICorner");
							local c = Instance.new("TextBox");
							r.Name = string.lower(X.Title);
							r.Parent = a;
							r.BackgroundColor3 = Color3.fromRGB(60, 60, 60);
							r.BackgroundTransparency = 1.0;
							r.Position = UDim2.new(0, 0, .208333328, 0);
							r.Size = UDim2.new(1, 0, 0, 50);
							m.CornerRadius = UDim.new(0, 4);
							m.Name = "SliderCorner";
							m.Parent = r;
							t.Name = "Background1";
							t.Parent = r;
							t.AnchorPoint = Vector2.new(.5, .5);
							t.Position = UDim2.new(.5, 0, .5, 0);
							t.Size = UDim2.new(1, -10, 1, 0);
							t.BackgroundColor3 = G.UIColor["Background 1 Color"];
							t.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
							i.CornerRadius = UDim.new(0, 4);
							i.Name = "SliderBGCorner";
							i.Parent = t;
							D.Name = "TextColor";
							D.Parent = t;
							D.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
							D.BackgroundTransparency = 1.0;
							D.Position = UDim2.new(0, 10, 0, 0);
							D.Size = UDim2.new(1, -10, 0, 25);
							D.Font = Enum.Font.GothamBlack;
							D.Text = I;
							D.TextSize = 14.0;
							D.TextXAlignment = Enum.TextXAlignment.Left;
							D.TextColor3 = G.UIColor["Text Color"];
							p.Name = "SliderBar";
							p.Parent = r;
							p.AnchorPoint = Vector2.new(.5, .5);
							p.Position = UDim2.new(.5, 0, .5, 14);
							p.Size = UDim2.new(1, -20, 0, 6);
							p.BackgroundColor3 = G.UIColor["Background 2 Color"];
							S.Name = "SliderButton ";
							S.Parent = p;
							S.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
							S.BackgroundTransparency = 1.0;
							S.Size = UDim2.new(1, 0, 1, 0);
							S.Font = Enum.Font.GothamBold;
							S.Text = "";
							S.TextColor3 = Color3.fromRGB(230, 230, 230);
							S.TextSize = 14.0;
							U.CornerRadius = UDim.new(1, 0);
							U.Name = "SliderBarCorner";
							U.Parent = p;
							b.Name = "Bar";
							b.BorderSizePixel = 0;
							b.Parent = p;
							b.Size = UDim2.new(0, 0, 1, 0);
							b.BackgroundColor3 = G.UIColor["Slider Line Color"];
							F.CornerRadius = UDim.new(1, 0);
							F.Name = "BarCorner";
							F.Parent = b;
							j.Name = "Background2";
							j.Parent = r;
							j.AnchorPoint = Vector2.new(1, 0);
							j.Position = UDim2.new(1, -10, 0, 5);
							j.Size = UDim2.new(0, 150, 0, 25);
							j.BackgroundColor3 = G.UIColor["Background 2 Color"];
							n.CornerRadius = UDim.new(0, 4);
							n.Name = "Sliderbox";
							n.Parent = j;
							c.Name = "TextColor";
							c.Parent = j;
							c.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
							c.BackgroundTransparency = 1.0;
							c.Size = UDim2.new(1, 0, 1, 0);
							c.Font = Enum.Font.GothamBold;
							c.Text = "";
							c.TextSize = 14.0;
							c.TextColor3 = G.UIColor["Text Color"];
							S.MouseEnter:Connect(function()
								(C:Create(b, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { BackgroundColor3 = G.UIColor["Slider Highlight Color"] })):Play();
							end);
							S.MouseLeave:Connect(function()
								(C:Create(b, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { BackgroundColor3 = G.UIColor["Slider Line Color"] })):Play();
							end);
							local l = function(G)
									c.Text = G;
									E[M].Default = G;
									f(M, X);
								end;
							if s then
								if s <= Y then
									s = Y;
								elseif s >= u then
									s = u;
								end;
								b.Size = UDim2.new(1 - (u - s) / (u - Y), 0, 0, 6);
								l(s);
							end;
							if A then
								local G = false;
								local M;
								local X = 0;
								local I = 0;
								local function s(M)
									if M.UserInputType == Enum.UserInputType.MouseButton1 or M.UserInputType == Enum.UserInputType.Touch then
										I = tick();
										M.Changed:Connect(function()
											if M.UserInputState == Enum.UserInputState.End then
												G = false;
												I = 0;
											end;
										end);
									end;
								end;
								local function r(M)
									if M.UserInputType == Enum.UserInputType.MouseButton1 or M.UserInputType == Enum.UserInputType.Touch then
										G = false;
										I = 0;
									end;
								end;
								local function C(G)
									if G.UserInputType == Enum.UserInputType.MouseMovement or G.UserInputType == Enum.UserInputType.Touch then
										M = G;
									end;
								end;
								S.InputBegan:Connect(s);
								S.InputEnded:Connect(r);
								S.InputChanged:Connect(C);
								R.RenderStepped:Connect(function()
									if I > 0 and (tick() - I >= X and not G) then
										G = true;
									end;
									if G and M then
										local G = P and tonumber(string.format("%.1f", ((tonumber(u) - tonumber(Y)) / w) * b.AbsoluteSize.X + tonumber(Y))) or math.floor(((tonumber(u) - tonumber(Y)) / w) * b.AbsoluteSize.X + tonumber(Y));
										pcall(function()
											l(G);
										end);
										b.Size = UDim2.new(0, math.clamp(M.Position.X - b.AbsolutePosition.X, 0, w), 0, 6);
									end;
								end);
							else
								local G = false;
								local M;
								local X = 0;
								local I = 0;
								local function s(M)
									if M.UserInputType == Enum.UserInputType.MouseButton1 or M.UserInputType == Enum.UserInputType.Touch then
										I = tick();
										M.Changed:Connect(function()
											if M.UserInputState == Enum.UserInputState.End then
												G = false;
												I = 0;
											end;
										end);
									end;
								end;
								local function r(M)
									if M.UserInputType == Enum.UserInputType.MouseButton1 or M.UserInputType == Enum.UserInputType.Touch then
										G = false;
										I = 0;
									end;
								end;
								local function C(G)
									if G.UserInputType == Enum.UserInputType.MouseMovement or G.UserInputType == Enum.UserInputType.Touch then
										M = G;
									end;
								end;
								S.InputBegan:Connect(s);
								S.InputEnded:Connect(r);
								S.InputChanged:Connect(C);
								R.RenderStepped:Connect(function()
									if I > 0 and (tick() - I >= X and not G) then
										G = true;
									end;
									if G and M then
										local G = P and tonumber(string.format("%.1f", ((tonumber(u) - tonumber(Y)) / w) * b.AbsoluteSize.X + tonumber(Y))) or math.floor(((tonumber(u) - tonumber(Y)) / w) * b.AbsoluteSize.X + tonumber(Y));
										pcall(function()
											l(G);
										end);
										b.Size = UDim2.new(0, math.clamp(M.Position.X - b.AbsolutePosition.X, 0, w), 0, 6);
									end;
								end);
							end;
							local function o(G)
								if tonumber(G) <= Y then
									b.Size = UDim2.new(0, 0 * w, 0, 6);
									l(Y);
								elseif tonumber(G) >= u then
									b.Size = UDim2.new(0, (u / u) * w, 0, 6);
									l(u);
								else
									b.Size = UDim2.new(1 - (u - G) / (u - Y), 0, 0, 6);
									l(G);
								end;
							end;
							c.FocusLost:Connect(function()
								o(c.Text);
							end);
						end;
					else
						for M, X in i(E) do
							if typeof(X) == "string" then
								local M = Instance.new("Frame");
								local Y = Instance.new("UICorner");
								local u = Instance.new("Frame");
								local s = Instance.new("UICorner");
								local w = Instance.new("TextLabel");
								local r = Instance.new("ImageButton");
								local A = Instance.new("TextButton");
								M.Name = string.lower(X);
								M.Parent = a;
								M.BackgroundColor3 = Color3.fromRGB(60, 60, 60);
								M.BackgroundTransparency = 1.0;
								M.BorderColor3 = Color3.fromRGB(27, 42, 53);
								M.LayoutOrder = 1;
								M.Position = UDim2.new(0, 0, .208333328, 0);
								M.Size = UDim2.new(1, 0, 0, 25);
								Y.CornerRadius = UDim.new(0, 4);
								Y.Name = "SampleItemCorner";
								Y.Parent = M;
								u.Name = "SampleItemBG";
								u.Parent = M;
								u.AnchorPoint = Vector2.new(.5, .5);
								u.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
								u.BackgroundTransparency = 1;
								u.BorderColor3 = Color3.fromRGB(27, 42, 53);
								u.Position = UDim2.new(.5, 0, .5, 0);
								u.Size = UDim2.new(1, 0, 1, 0);
								s.CornerRadius = UDim.new(0, 4);
								s.Name = "SampleItemBGCorner";
								s.Parent = u;
								w.Name = "SampleItemTitle";
								w.Parent = u;
								w.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
								w.BackgroundTransparency = 1.0;
								w.BorderColor3 = Color3.fromRGB(27, 42, 53);
								w.Position = UDim2.new(0, 10, 0, 0);
								w.Size = UDim2.new(1, -40, 0, 25);
								w.Font = Enum.Font.GothamBlack;
								w.Text = X;
								w.TextColor3 = Color3.fromRGB(255, 255, 255);
								w.TextSize = 14.0;
								w.TextStrokeTransparency = .5;
								w.TextXAlignment = Enum.TextXAlignment.Left;
								r.Name = "SampleItemCheck";
								r.Parent = u;
								r.AnchorPoint = Vector2.new(1, .5);
								r.BackgroundTransparency = 1.0;
								r.Position = UDim2.new(1, 0, .5, 0);
								r.Size = UDim2.new(0, 25, 0, 25);
								r.ZIndex = 2;
								r.Image = "rbxassetid://3926305904";
								r.ImageColor3 = G.UIColor["Dropdown Selected Check Color"];
								r.ImageRectOffset = Vector2.new(312, 4);
								r.ImageRectSize = Vector2.new(24, 24);
								r.ImageTransparency = 1;
								A.Name = "SampleItemButton";
								A.Parent = M;
								A.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
								A.BackgroundTransparency = 1.0;
								A.BorderColor3 = Color3.fromRGB(0, 0, 0);
								A.BorderSizePixel = 0;
								A.Size = UDim2.new(1, 0, 1, 0);
								A.Font = Enum.Font.SourceSans;
								A.TextColor3 = G.UIColor["Text Color"];
								A.TextSize = 14.0;
								A.TextTransparency = 1.0;
								A.MouseEnter:Connect(function()
									if W.Value == X then
										return;
									end;
									(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundColor3 = Color3.fromRGB(255, 255, 255) })):Play();
									(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = .7 })):Play();
								end);
								A.MouseLeave:Connect(function()
									if W.Value == X then
										return;
									end;
									(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundColor3 = Color3.fromRGB(255, 255, 255) })):Play();
									(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = 1 })):Play();
								end);
								A.MouseButton1Click:Connect(function()
									if P then
										J.PlaceholderText = I .. (": " .. X) or "";
										W.Value = X;
									else
										J.Text = I .. (": " .. X) or "";
										W.Value = X;
									end;
									(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundColor3 = G.UIColor["Dropdown Selected Check Color"] })):Play();
									(C:Create(u, TweenInfo.new(G.UIColor["Tween Animation 1 Speed"]), { BackgroundTransparency = .5 })):Play();
									if f then
										f(X);
									end;
									if P then
										J.Text = "";
									end;
									y();
								end);
								if W.Value == X then
									u.BackgroundTransparency = .5;
									u.BackgroundColor3 = G.UIColor["Dropdown Selected Check Color"];
									M.LayoutOrder = 0;
								end;
							end;
						end;
					end;
				end;
				if P then
					J.Changed:Connect(function()
						x();
						d();
					end);
				end;
				if typeof(m) ~= "table" then
					f(m);
					if P then
						J.PlaceholderText = I .. (": " .. tostring(m or ""));
					else
						J.Text = I .. (": " .. tostring(m or ""));
					end;
				elseif r then
					J.Text = "";
					J.PlaceholderText = I .. ": ";
				elseif s then
					if P then
						J.PlaceholderText = I .. ": ";
					else
						J.Text = I .. ": ";
					end;
				end;
				j.MouseButton1Click:Connect(function()
					y();
					v = not v;
					local M = v and UDim2.new(1, 0, 0, 170) or UDim2.new(1, 0, 0, 0);
					local X = v and UDim2.new(1, 0, 0, 200) or UDim2.new(1, 0, 0, 25);
					local I = v and 90 or 0;
					(C:Create(n, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Size = M })):Play();
					(C:Create(D, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Size = X })):Play();
					(C:Create(F, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Rotation = I })):Play();
				end);
				local g = { rf = y };
				function g.ClearText(M, G)
					if not s then
						if P then
							J.PlaceholderText = I .. (": " .. (G or ""));
						else
							J.Text = I .. (": " .. (G or ""));
						end;
					else
						J.Text = I .. (": " .. (G or ""));
					end;
				end;
				function g.GetNewList(X, M)
					W.Value = "";
					v = false;
					local Y = v and UDim2.new(1, 0, 0, 170) or UDim2.new(1, 0, 0, 0);
					local u = v and UDim2.new(1, 0, 0, 200) or UDim2.new(1, 0, 0, 25);
					local s = v and 90 or 0;
					(C:Create(n, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Size = Y })):Play();
					(C:Create(D, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Size = u })):Play();
					(C:Create(F, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { Rotation = s })):Play();
					E = {};
					E = M;
					y();
					if P then
						J.PlaceholderText = I .. ": ";
					else
						J.Text = I .. ": ";
					end;
				end;
				table.insert(G.listfunction[w], { Type = "Dropdown", Name = I, Call = function()
						D.Visible = true;
					end });
				table.insert(u[w], D);
				return g;
			end;
			function j.CreateBind(M, X)
				local I = tostring(M.Title) or "";
				table.insert(G.listfunction[w], { Type = "Bind", Name = I });
				local Y = M.Key;
				local u = M.Default or M.Key;
				local P = (tostring(u)):match("UserInputType") and "UserInputType" or "KeyCode";
				local s = X or function()
 
					end;
				Y = (tostring(Y)):gsub("Enum.UserInputType.", "");
				Y = (tostring(Y)):gsub("Enum.KeyCode.", "");
				local r = Instance.new("Frame");
				local C = Instance.new("UICorner");
				local A = Instance.new("Frame");
				local R = Instance.new("UICorner");
				local m = Instance.new("TextLabel");
				local f = Instance.new("TextButton");
				local t = Instance.new("Frame");
				local i = Instance.new("UICorner");
				local D = Instance.new("TextButton");
				r.Name = I .. "bguvl";
				r.Parent = w;
				r.BackgroundColor3 = Color3.fromRGB(60, 60, 60);
				r.BackgroundTransparency = 1.0;
				r.Position = UDim2.new(0, 0, .208333328, 0);
				r.Size = UDim2.new(1, 0, 0, 35);
				C.CornerRadius = UDim.new(0, 4);
				C.Name = "BindCorner";
				C.Parent = r;
				A.Name = "Background1";
				A.Parent = r;
				A.AnchorPoint = Vector2.new(.5, .5);
				A.Position = UDim2.new(.5, 0, .5, 0);
				A.Size = UDim2.new(1, -10, 1, 0);
				A.BackgroundColor3 = G.UIColor["Background 1 Color"];
				A.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
				R.CornerRadius = UDim.new(0, 4);
				R.Name = "ButtonCorner";
				R.Parent = A;
				m.Name = "TextColor";
				m.Parent = A;
				m.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				m.BackgroundTransparency = 1.0;
				m.Position = UDim2.new(0, 10, 0, 0);
				m.Size = UDim2.new(1, -10, 1, 0);
				m.Font = Enum.Font.GothamBlack;
				m.Text = I;
				m.TextSize = 14.0;
				m.TextXAlignment = Enum.TextXAlignment.Left;
				m.TextColor3 = G.UIColor["Text Color"];
				t.Name = "Background2";
				t.Parent = A;
				t.AnchorPoint = Vector2.new(1, .5);
				t.Position = UDim2.new(1, -5, .5, 0);
				t.Size = UDim2.new(0, 150, 0, 25);
				t.BackgroundColor3 = G.UIColor["Background 2 Color"];
				i.CornerRadius = UDim.new(0, 4);
				i.Name = "ButtonCorner";
				i.Parent = t;
				D.Name = "Bindkey";
				D.Parent = t;
				D.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				D.BackgroundTransparency = 1.0;
				D.Size = UDim2.new(1, 0, 1, 0);
				D.Font = Enum.Font.GothamBold;
				D.Text = (tostring(u)):gsub("Enum.KeyCode.", "");
				D.TextSize = 14.0;
				D.TextColor3 = G.UIColor["Text Color"];
				local p = { [Enum.UserInputType.MouseButton1] = "Mouse1", [Enum.UserInputType.MouseButton2] = "Mouse2", [Enum.UserInputType.MouseButton3] = "Mouse3" };
				D.MouseButton1Click:Connect(function()
					local G;
					D.Text = "...";
					G = (game:GetService("UserInputService")).InputBegan:Connect(function(M)
							if p[M.UserInputType] then
								D.Text = p[M.UserInputType];
								spawn(function()
									wait(.1);
									u = M.UserInputType;
									P = "UserInputType";
								end);
							elseif M.KeyCode ~= Enum.KeyCode.Unknown then
								D.Text = (tostring(M.KeyCode)):gsub("Enum.KeyCode.", "");
								spawn(function()
									wait(.1);
									u = M.KeyCode;
									P = "KeyCode";
								end);
							end;
							G:Disconnect();
						end);
				end);
				(game:GetService("UserInputService")).InputBegan:Connect(function(G)
					if u == G.UserInputType or u == G.KeyCode then
						s(u);
					end;
				end);
			end;
			function j.CreateBox(M, X)
				local I = tostring(M.Title) or "";
				local Y = tostring(M.Placeholder) or "";
				local P = M.Default or false;
				local s = M.Number or false;
				local r = X or function()
 
					end;
				local A = Instance.new("Frame");
				local R = Instance.new("UICorner");
				local m = Instance.new("Frame");
				local f = Instance.new("UICorner");
				local t = Instance.new("TextLabel");
				local i = Instance.new("Frame");
				local D = Instance.new("UICorner");
				local p = Instance.new("TextBox");
				local S = Instance.new("Frame");
				local U = Instance.new("UICorner");
				A.Name = "BoxFrame";
				A.Parent = w;
				A.BackgroundColor3 = Color3.fromRGB(60, 60, 60);
				A.BackgroundTransparency = 1.0;
				A.Position = UDim2.new(0, 0, .208333328, 0);
				A.Size = UDim2.new(1, 0, 0, 60);
				R.CornerRadius = UDim.new(0, 4);
				R.Name = "BoxCorner";
				R.Parent = A;
				m.Name = "Background1";
				m.Parent = A;
				m.AnchorPoint = Vector2.new(.5, .5);
				m.Position = UDim2.new(.5, 0, .5, 0);
				m.Size = UDim2.new(1, -10, 1, 0);
				m.BackgroundColor3 = G.UIColor["Background 1 Color"];
				m.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
				f.CornerRadius = UDim.new(0, 4);
				f.Name = "ButtonCorner";
				f.Parent = m;
				t.Name = "TextColor";
				t.Parent = m;
				t.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				t.BackgroundTransparency = 1.0;
				t.Position = UDim2.new(0, 10, 0, 0);
				t.Size = UDim2.new(1, -10, .5, 0);
				t.Font = Enum.Font.GothamBlack;
				t.Text = I;
				t.TextSize = 14.0;
				t.TextXAlignment = Enum.TextXAlignment.Left;
				t.TextColor3 = G.UIColor["Text Color"];
				i.Name = "Background2";
				i.Parent = m;
				i.AnchorPoint = Vector2.new(1, .5);
				i.ClipsDescendants = true;
				i.Position = UDim2.new(1, -5, 0, 40);
				i.Size = UDim2.new(1, -10, 0, 25);
				i.BackgroundColor3 = G.UIColor["Background 2 Color"];
				D.CornerRadius = UDim.new(0, 4);
				D.Name = "ButtonCorner";
				D.Parent = i;
				p.Name = "TextColorPlaceholder";
				p.Parent = i;
				p.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				p.BackgroundTransparency = 1.0;
				p.Position = UDim2.new(0, 5, 0, 0);
				p.Size = UDim2.new(1, -5, 1, 0);
				p.Font = Enum.Font.GothamBold;
				p.PlaceholderText = Y;
				p.Text = "";
				p.TextSize = 14.0;
				p.TextXAlignment = Enum.TextXAlignment.Left;
				p.PlaceholderColor3 = G.UIColor["Placeholder Text Color"];
				p.TextColor3 = G.UIColor["Text Color"];
				S.Name = "TextNSBoxLineeeee";
				S.Parent = i;
				S.BackgroundTransparency = 1.0;
				S.Position = UDim2.new(0, 0, 1, -2);
				S.Size = UDim2.new(1, 0, 0, 6);
				S.BackgroundColor3 = G.UIColor["Box Highlight Color"];
				U.CornerRadius = UDim.new(1, 0);
				U.Parent = S;
				p.Focused:Connect(function()
					(C:Create(S, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { BackgroundTransparency = 0 })):Play();
				end);
				if s then
					(p:GetPropertyChangedSignal("Text")):Connect(function()
						if tonumber(p.Text) then
 
						else
							p.PlaceholderText = Y;
							p.Text = "";
						end;
					end);
				end;
				p.FocusLost:Connect(function()
					(C:Create(S, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { BackgroundTransparency = 1 })):Play();
					if p.Text ~= "" then
						r(p.Text);
					end;
				end);
				local b = {};
				if P then
					p.Text = P;
					r(P);
				end;
				function b.SetValue(G)
					p.Text = G;
					r(G);
				end;
				table.insert(G.listfunction[w], { Type = "Box", Name = I, Call = function()
						A.Visible = true;
					end });
				table.insert(u[w], A);
				return b;
			end;
			function j.CreateSlider(M, X)
				local I = tostring(M.Title) or "";
				local Y = tonumber(M.Min) or 0;
				local P = tonumber(M.Max) or 100;
				local s = M.Precise or false;
				local r = tonumber(M.Default) or 0;
				local A = X or function()
 
					end;
				local m = 400;
				local f = A or function()
 
					end;
				local t = Instance.new("Frame");
				local i = Instance.new("UICorner");
				local D = Instance.new("Frame");
				local p = Instance.new("UICorner");
				local S = Instance.new("TextLabel");
				local U = Instance.new("Frame");
				local b = Instance.new("TextButton");
				local F = Instance.new("UICorner");
				local j = Instance.new("Frame");
				local n = Instance.new("UICorner");
				local c = Instance.new("Frame");
				local a = Instance.new("UICorner");
				local l = Instance.new("TextBox");
				t.Name = I .. "buda";
				t.Parent = w;
				t.BackgroundColor3 = Color3.fromRGB(60, 60, 60);
				t.BackgroundTransparency = 1.0;
				t.Position = UDim2.new(0, 0, .208333328, 0);
				t.Size = UDim2.new(1, 0, 0, 50);
				i.CornerRadius = UDim.new(0, 4);
				i.Name = "SliderCorner";
				i.Parent = t;
				D.Name = "Background1";
				D.Parent = t;
				D.AnchorPoint = Vector2.new(.5, .5);
				D.Position = UDim2.new(.5, 0, .5, 0);
				D.Size = UDim2.new(1, -10, 1, 0);
				D.BackgroundColor3 = G.UIColor["Background 1 Color"];
				D.BackgroundTransparency = G.UIColor["Background 1 Transparency"];
				p.CornerRadius = UDim.new(0, 4);
				p.Name = "SliderBGCorner";
				p.Parent = D;
				S.Name = "TextColor";
				S.Parent = D;
				S.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				S.BackgroundTransparency = 1.0;
				S.Position = UDim2.new(0, 10, 0, 0);
				S.Size = UDim2.new(1, -10, 0, 25);
				S.Font = Enum.Font.GothamBlack;
				S.Text = I;
				S.TextSize = 14.0;
				S.RichText = true;
				S.TextXAlignment = Enum.TextXAlignment.Left;
				S.TextColor3 = G.UIColor["Text Color"];
				U.Name = "SliderBar";
				U.Parent = t;
				U.AnchorPoint = Vector2.new(.5, .5);
				U.Position = UDim2.new(.5, 0, .5, 14);
				U.Size = UDim2.new(0, 400, 0, 6);
				U.BackgroundColor3 = G.UIColor["Background 2 Color"];
				b.Name = "SliderButton ";
				b.Parent = U;
				b.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				b.BackgroundTransparency = 1.0;
				b.Size = UDim2.new(1, 0, 1, 0);
				b.Font = Enum.Font.GothamBold;
				b.Text = "";
				b.TextColor3 = Color3.fromRGB(230, 230, 230);
				b.TextSize = 14.0;
				F.CornerRadius = UDim.new(1, 0);
				F.Name = "SliderBarCorner";
				F.Parent = U;
				j.Name = "Bar";
				j.BorderSizePixel = 0;
				j.Parent = U;
				j.Size = UDim2.new(0, 0, 1, 0);
				j.BackgroundColor3 = G.UIColor["Slider Line Color"];
				n.CornerRadius = UDim.new(1, 0);
				n.Name = "BarCorner";
				n.Parent = j;
				c.Name = "Background2";
				c.Parent = t;
				c.AnchorPoint = Vector2.new(1, 0);
				c.Position = UDim2.new(1, -10, 0, 5);
				c.Size = UDim2.new(0, 150, 0, 25);
				c.BackgroundColor3 = G.UIColor["Background 2 Color"];
				a.CornerRadius = UDim.new(0, 4);
				a.Name = "Sliderbox";
				a.Parent = c;
				l.Name = "TextColor";
				l.Parent = c;
				l.BackgroundColor3 = Color3.fromRGB(230, 230, 230);
				l.BackgroundTransparency = 1.0;
				l.Size = UDim2.new(1, 0, 1, 0);
				l.Font = Enum.Font.GothamBold;
				l.Text = "";
				l.TextSize = 14.0;
				l.TextColor3 = G.UIColor["Text Color"];
				b.MouseEnter:Connect(function()
					(C:Create(j, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { BackgroundColor3 = G.UIColor["Slider Highlight Color"] })):Play();
				end);
				b.MouseLeave:Connect(function()
					(C:Create(j, TweenInfo.new(G.UIColor["Tween Animation 2 Speed"]), { BackgroundColor3 = G.UIColor["Slider Line Color"] })):Play();
				end);
				local o = function(G)
						l.Text = G;
						f(tonumber(G));
					end;
				if r then
					if r <= Y then
						r = Y;
					elseif r >= P then
						r = P;
					end;
					j.Size = UDim2.new(1 - (P - r) / (P - Y), 0, 0, 6);
					o(r);
				end;
				local J = false;
				local W;
				local v = 0;
				local k = 0;
				local function z(G)
					if G.UserInputType == Enum.UserInputType.MouseButton1 or G.UserInputType == Enum.UserInputType.Touch then
						k = tick();
						G.Changed:Connect(function()
							if G.UserInputState == Enum.UserInputState.End then
								J = false;
								k = 0;
							end;
						end);
					end;
				end;
				local function x(G)
					if G.UserInputType == Enum.UserInputType.MouseButton1 or G.UserInputType == Enum.UserInputType.Touch then
						J = false;
						k = 0;
					end;
				end;
				local function d(G)
					if G.UserInputType == Enum.UserInputType.MouseMovement or G.UserInputType == Enum.UserInputType.Touch then
						W = G;
					end;
				end;
				b.InputBegan:Connect(z);
				b.InputEnded:Connect(x);
				b.InputChanged:Connect(d);
				R.RenderStepped:Connect(function()
					if k > 0 and (tick() - k >= v and not J) then
						J = true;
					end;
					if J and W then
						local G = s and tonumber(string.format("%.1f", ((tonumber(P) - tonumber(Y)) / m) * j.AbsoluteSize.X + tonumber(Y))) or math.floor(((tonumber(P) - tonumber(Y)) / m) * j.AbsoluteSize.X + tonumber(Y));
						pcall(function()
							o(G);
						end);
						j.Size = UDim2.new(0, math.clamp(W.Position.X - j.AbsolutePosition.X, 0, m), 0, 6);
					end;
				end);
				local function O(G)
					if tonumber(G) <= Y then
						j.Size = UDim2.new(0, 0 * m, 0, 6);
						o(Y);
					elseif tonumber(G) >= P then
						j.Size = UDim2.new(0, (P / P) * m, 0, 6);
						o(P);
					else
						j.Size = UDim2.new(1 - (P - G) / (P - Y), 0, 0, 6);
						o(G);
					end;
				end;
				l.FocusLost:Connect(function()
					O(l.Text);
				end);
				local E = {};
				function E.SetValue(G)
					O(G);
				end;
				table.insert(G.listfunction[w], { Type = "Slider", Name = I, Call = function()
						t.Visible = true;
					end });
				table.insert(u[w], t);
				return E;
			end;
			return j;
		end;
		return k;
	end;
	Y = function()
			for G, M in pairs(p:GetChildren()) do
				if not M:IsA("UIListLayout") then
					M.Visible = true;
				end;
			end;
			for G, M in pairs(b:GetChildren()) do
				if not M:IsA("UIPageLayout") and not M:IsA("UICorner") then
					M.Visible = true;
				end;
			end;
			for G, M in pairs(u) do
				G.Visible = true;
				for G, M in pairs(M) do
					M.Visible = true;
				end;
			end;
		end;
	(B:GetPropertyChangedSignal("Text")):Connect(function()
		local M = B.Text;
		if M == "" then
			Y();
		else
			for G, M in pairs(u) do
				G.Visible = false;
				for G, M in pairs(M) do
					M.Visible = false;
				end;
			end;
			for G, M in pairs(p:GetChildren()) do
				if not M:IsA("UIListLayout") then
					M.Visible = false;
				end;
			end;
			for G, M in pairs(b:GetChildren()) do
				if not M:IsA("UIPageLayout") and not M:IsA("UICorner") then
					M.Visible = false;
				end;
			end;
			for X, I in pairs(G.listfunction) do
				for I, Y in pairs(I) do
					if string.find(Y.Name:lower(), M:lower()) then
						if Y.Call then
							Y.Call();
						end;
						local M = G.listtab[X];
						if M then
							M[1].Visible = true;
							M[2].Visible = true;
							M[3].Visible = true;
							local X = G.UIColor["Tween Animation 1 Speed"];
							F.TweenTime = 0;
							F:JumpTo(M[2]);
							task.wait();
							F.TweenTime = X;
						end;
					end;
				end;
			end;
		end;
	end);
	return h;
end;
w.CreateNoti({ Title = "Notification", Desc = "The UI automatically hides once executed.\nPress the button at the bottom-left of the screen to show the GUI.", ShowTime = 10 }, true);
local U = w.CreateMain({ Desc = " _ng.shinichi" });
local b = U.CreatePage({ Page_Name = "Home", Page_Title = "Home" });
local F = U.CreatePage({ Page_Name = "Home1", Page_Title = "Home2" });
local j = U.CreatePage({ Page_Name = "Home3", Page_Title = "Home4" });
local n = b.CreateSection("Setting");
n.CreateToggle({ Title = "Enable/Disable function", Desc = "Here is an example toggle", Default = false }, function(G)
	print("Toggle state:", G);
end);
n.CreateButton({ Title = "Click me" }, function()
	print("Button has been pressed!");
end);
n.CreateLabel({ Title = "Here is an example label" });
n.CreateSlider({
	Title = "Adjust value",
	Min = 0,
	Max = 100,
	Default = 50,
	Precise = true,
}, function(G)
	print("Slider value:", G);
end);
n.CreateBox({
	Title = "Enter text",
	Placeholder = "Type something...",
	Default = "",
	Number = false,
}, function(G)
	print("You have entered:", G);
end);
n.CreateDropdown({
	Title = "Dropdown",
	List = { "Option 1", "Option 2", "Option 3" },
	Search = false,
	Selected = false,
	Default = "Option 1",
}, function(G)
	print(G);
end);
local c = F.CreateSection("Setting 2");
c.CreateToggle({ Title = "Enable/Disable function", Desc = "Here is an example toggle", Default = false }, function(G)
	print("Toggle state:", G);
end);
