# cairo-metro

Find the best route between any two Cairo Metro stations: which lines to take, where to change, how many stations, and the ticket price. Station names in Arabic and English.

> Status: early development.

## Planned features

- [ ] Station and line data for all Cairo Metro lines (Arabic + English names)
- [ ] Shortest route between two stations, with transfer points
- [ ] Ticket price based on the number of stations
- [ ] Fuzzy station search ("maadi", "المعادى", "el maadi")
- [ ] Command-line tool
- [ ] REST API (FastAPI)
- [ ] Simple web page
- [ ] Natural-language questions in Egyptian Arabic ("أروح من المرج للمعادي إزاي؟") using an LLM with the route API as a tool
- [ ] Automated tests for routes, transfers and prices

## Planned usage

```bash
cairo-metro route "El Marg" "Maadi"
```

```python
from cairo_metro import route

r = route("El Marg", "Maadi")
print(r.stations, r.transfers, r.price)
```

## Roadmap

1. Project setup: packaging, CLI, tests, CI
2. Station and line data
3. Route finding and transfers
4. Fare rules
5. Fuzzy station search
6. REST API
7. Web page
8. Natural-language questions
9. Docs and PyPI release

## Data note

Station and fare data is public information and must be checked against official sources before any real use. Fares change; this project is not an official source.

## License

MIT, see [LICENSE](LICENSE).

---
Built by [Hesham Ashraf](https://www.linkedin.com/in/hesham-ashrf)
