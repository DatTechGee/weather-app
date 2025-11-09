# Klimate Dattechgee - Modern Weather App ⛅

A modern weather forecast application built with cutting-edge technologies, featuring real-time weather data, beautiful UI, and seamless dark/light mode.

![DatTechGee Weather](public/logo-light.svg)

## 🌟 Features

- 🌤️ Real-time weather forecasts
- 🌙 Dark/Light mode with custom gradient themes
- 📱 Responsive design
- 📍 Location-based weather
- ⭐ Favorite locations
- 📊 Weather charts and statistics
- 🔍 City search with history
- 🌡️ Detailed weather metrics

## 🛠️ Core Technologies

- **Frontend**: React + TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **API**: OpenWeather API

## 📚 Key Libraries and Their Usage

### TanStack Query (React Query)
- Efficient API data fetching and caching
- Real-time weather updates with automatic background refetching
- Optimistic updates for favorites management
- Built-in loading and error states
```typescript
const { data, isLoading } = useQuery({
  queryKey: ['weather', city],
  queryFn: () => fetchWeatherData(city)
});
```

### React Router DOM
- Dynamic routing for city-specific weather pages
- Clean URLs with city names
- Search history management
```typescript
// Route definitions
<Route path="/city/:cityName" element={<CityPage />} />

// Navigation
navigate(`/city/${cityName}`);
```

### Recharts
- Interactive weather charts and graphs
- Temperature trend visualization
- Precipitation and humidity charts
- Responsive design adaptation
```typescript
<LineChart data={hourlyData}>
  <Line type="monotone" dataKey="temp" stroke="#8884d8" />
  <XAxis dataKey="time" />
  <YAxis />
  <Tooltip />
</LineChart>
```

### Radix UI
- Accessible component primitives
- Used throughout the app:
  - Dialog: City search modal
  - DropdownMenu: Settings and options
  - ScrollArea: Long lists of cities
  - Switch: Theme toggler
  - Tooltip: UI element descriptions
```typescript
<Dialog.Root>
  <Dialog.Trigger>Search Cities</Dialog.Trigger>
  <Dialog.Content>
    <SearchForm />
  </Dialog.Content>
</Dialog.Root>
```

### Lucide React
- Modern icon system
- Weather condition icons
- Navigation and UI element icons
- Consistent styling across the app
```typescript
import { Cloud, Sun, Wind } from 'lucide-react';

// Usage in components
<Sun className="h-6 w-6" />
```

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone https://github.com/yourusername/weather-forecast.git
cd weather-forecast
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory:
```env
VITE_OPENWEATHER_API_KEY=your_api_key_here
VITE_OPENWEATHER_API_KEY=8d06c66968f4f38ec8412c35a26fad08
```

4. Start the development server:
```bash
npm run dev
```

Visit `http://localhost:5173` to see the app in action!

## 🎨 Customization

- Edit theme colors in `src/index.css`
- Modify components in `src/components`
- Adjust API calls in `src/api`

## 📝 License

MIT © [DatTechGee]

## 🙏 Credits

Built with ❤️ by DatTechGee
