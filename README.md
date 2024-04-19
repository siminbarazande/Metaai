# MetaAI API Wrapper

MetaAI is a Python library designed to interact with Meta's AI APIs that run in the backend of https://www.meta.ai/. It encapsulates the complexities of authentication and communication with the APIs, providing a straightforward interface for sending queries and receiving responses.

With this you can easily prompt the AI with a message and get a response, directly from your Python code. **NO API KEY REQUIRED**

**Meta AI is connected to the internet, so you will be able to get the latest real-time responses from the AI.** (powered by Bing)

Meta AI is running Llama 3 LLM.

## Usage
**Download**:

   ```bash
   pip install meta-ai-api
   ```
   
**Initialization**:

```python
from meta_ai_api import MetaAI

ai = MetaAI()
response = ai.prompt(message="Whats the weather in San Francisco today? And what is the date?")
print(response)
 
```
result:
```json
{
   "message":"The weather in San Francisco, California, today includes ¹:\nNo precipitation with skies ranging from clear to cloudy\nWind speeds range from 0 to 21 miles per hour\nTemperatures range from 52 to 69 degrees Fahrenheit\nPlease note that the weather forecast is continually changing ² ³ ⁴.\n",
   "sources":[
      {
         "link":"https://www.wolframalpha.com/input?i=San+Francisco+weather+today",
         "title":"WolframAlpha"
      },
      {
         "link":"https://www.accuweather.com/en/us/san-francisco/94103/weather-forecast/347629",
         "title":"San Francisco, CA Weather Forecast - AccuWeather"
      },
      {
         "link":"https://weather.com/weather/tenday/l/San+Francisco+CA+USCA0987:1:US",
         "title":"10-Day Weather Forecast for San Francisco, CA"
      },
      {
         "link":"https://weather.com/weather/tenday/l/Inverness+CA?canonicalCityId=61b2ebcaa5e78eebca92d21eaff7a0439eb081e8e60287fca37af4186f8242b7",
         "title":"10-Day Weather Forecast for Inverness, CA"
      }
   ]
}
```

```python
from meta_ai_api import MetaAI

ai = MetaAI()
response = ai.prompt(message="What was the Warriors score last game?")
print(response)
```
result:
```json
{
   "message":"The Golden State Warriors' last game was against the Sacramento Kings, and they lost 118-94 ¹ ². Stephen Curry scored 22 points, and the Kings' win eliminated the Warriors from the playoffs ³. The Warriors finished the season 46-36 and 10th in the Western Conference ⁴ ³.\n",
   "sources":[
      {
         "link":"https://sportradar.com/",
         "title":"Game Info of NBA from sportradar.com"
      },
      {
         "link":"https://www.sofascore.com/team/basketball/golden-state-warriors/3428",
         "title":"Golden State Warriors live scores & schedule - Sofascore"
      },
      {
         "link":"https://www.foxsports.com/nba/golden-state-warriors-team-schedule",
         "title":"Golden State Warriors Schedule & Scores - NBA - FOX Sports"
      },
      {
         "link":"https://en.wikipedia.org/wiki/History_of_the_Golden_State_Warriors",
         "title":"History of the Golden State Warriors"
      }
   ]
}
```
