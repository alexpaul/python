# Agents

## Snippet of an agent

```python
# Here we get the coordinates of a given location, the weather and send an email to a recipient
weather_agent = Agent(
    name="Weather Agent",
    instructions="You are a helpful agent.",
    functions=[get_coordinates, get_weather, send_email]
)
```

## Prompt 

> Include the current weather for Saint Lucia in the email, along with the top 10 things to do there.


## Output

```
Sending email...
To: recipient@example.com
Subject: Weather and Top Things to Do in Saint Lucia
Body: Here is the current weather in Soufrière, Saint Lucia:

- Temperature: 75.47°F
- Humidity: 69%
- Wind Speed: 19.77 mph
- Conditions: Clear sky

Top 10 Things to Do in Saint Lucia:
1. Visit the Pitons - These iconic volcanic peaks are a UNESCO World Heritage site and offer stunning hiking opportunities.
2. Sulphur Springs Park - Explore the world's only drive-in volcano and take a rejuvenating mud bath.
3. Diamond Falls Botanical Gardens - Enjoy the beautiful gardens and the stunning Diamond Waterfall.
4. Pigeon Island National Park - Discover the historical ruins and enjoy hiking trails with breathtaking sea views.
5. Marigot Bay - This scenic bay is perfect for sailing, dining, and enjoying picturesque views.
6. Anse Chastanet - A beautiful beach known for its excellent snorkeling and diving spots.
7. Castries Market - Experience vibrant local culture and shop for handmade crafts and fresh produce.
8. Gros Islet Street Party - Join in this famous Friday night street party for music, dancing, and local food.
9. Rodney Bay - Explore the marina, beautiful beaches, and enjoy dining and nightlife.
10. Moule a Chique - Climb to the top of this hill for panoramic views over the island and the nearby island of St. Vincent.
```

***

## Resources 

* [OpenAI: Swarm](https://github.com/openai/swarm/tree/main)
