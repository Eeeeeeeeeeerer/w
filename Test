local HttpService = game:GetService("HttpService")

local function getRandomJoke()
    local success, response = pcall(function()
        return HttpService:GetAsync("https://official-joke-api.appspot.com/random_joke")
    end)

    if success then
        local jokeData = HttpService:JSONDecode(response)
        print("Joke:", jokeData.setup)
        print("Punchline:", jokeData.punchline)
    else
        warn("Failed to get joke:", response)
    end
end

getRandomJoke()
