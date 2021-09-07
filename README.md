# assignment2-Jupally
# Jupally Kavya
###### HYDERABAD

Hyderabad is among the most developed Indian cities. The city of Hyderabad is famous for its  rich architecture, culture & history.Hyderabad is also known for its unique features of meeting point of Southern & Northern parts of India.Hyderabad is a beautiful city known for its joy and love. The residents of the city have intrinsic goodness and charm. This is the reason Hyderabad is famous for its Hospitality. The unique feature of the city is that it follows both the ancient cultures and high tech economy. **I love my city** a lot and I recommend everybody to visit my city once and experience its beauty and culture.

---

# Directions from Maryville to Nevada
1. Catch a directions of 1,396 miles from marryville to Henderson via flight
2. catch a cab and go to the kansas airport(mca)
    1. take a flight from kansas to lasvegas airport(las)
    2. take all ur belongings and book a cab to henderson which takes 10-15 min from airport
3. wait for the cab to arive 
    1. Sit back and enjoy the lightning and mountain view 
    2. By listening to ur favourit music
4. Finally we have reached our location yeyeye..!!


* Items i would like to carry with me:
 * Drinks:
    * Cocola
    * Tropicana
    * Minute maid
    * Water 
* Accessories:
    * Airpods
    * iwatch
    * DSLR
    * Power Bank  
    * Cable 
* Snacks  
    * Chocolates
    * Chips

**[AboutMe.md](AboutMe.md)**

---

# food i loved and i would love to suggest
I am going to create a table with  4 food items that I would love to recommend someone try = Thai Friedrice, Pizza,Sushi , Icecream.

|Food Item|Location| Cost|
|---|---|---|
|Thai Friedrice|rewoke|10$|
|Pizza|Pizzeria|7$|
|Sushi|Republica|12$|
|Icecream|creamworld|2$|


# Pithy Quote

> "When nobody else celebrates you, learn to celebrate yourself. When nobody else compliments you, then compliment yourself. It’s not up to other people to keep you encouraged. It’s up to you. Encouragement should come from the inside." *Jay Shetty*
<Br>
> "Hell is empty and all the devils are here." *William Shakespeare*


---
# Dijkstra Algorithm
> Dijkstra's algorithm is an algorithm for finding the shortest paths between nodes in a graph, which may represent, for example, road networks. It was conceived by computer scientist Edsger W. Dijkstra in 1956 and published three years later. The algorithm exists in many variant

[Click Here to Know More](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)


```

const int INF = 1000000000;
vector<vector<pair<int, int>>> adj;

void dijkstra(int s, vector<int> & d, vector<int> & p) {
    int n = adj.size();
    d.assign(n, INF);
    p.assign(n, -1);
    vector<bool> u(n, false);

    d[s] = 0;
    for (int i = 0; i < n; i++) {
        int v = -1;
        for (int j = 0; j < n; j++) {
            if (!u[j] && (v == -1 || d[j] < d[v]))
                v = j;
        }

        if (d[v] == INF)
            break;

        u[v] = true;
        for (auto edge : adj[v]) {
            int to = edge.first;
            int len = edge.second;

            if (d[v] + len < d[to]) {
                d[to] = d[v] + len;
                p[to] = v;
            }
        }
    }
}
```
[code source](https://cp-algorithms.com/graph/dijkstra.html)

