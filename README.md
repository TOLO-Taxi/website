# Mobile App Landing Page

## 💡 Features

Mobile App Landing Page Template comes with pre-installed features and options:

- Display app icon
- Show unlimited app screenshots
- Link to Google Play
- Link to the AppStore
- Link to the Web App
- Press mention section
- Product Hunt floating prompt
- Privacy policy Page
- Google Analytics
- Cookie Consent
- Automatic dark theme
- Doorbell widget
- Github forking banner

## 📖 How to use

### The normal way

1. Fork this project
2. Edit `_config.yml`, feel free to commut/uncomment what you need (google analtytics, or github for example)
3. Edit `_data/app.yml` with your app data
4. Update the text from `_data/strings.yml`, you can customize there the footer's links
5. Edit icons and screenshots inside the `_images` folder and `icon.png` in the root
6. Edit `_src/index.js` to update the product hunt modal (or to remove it) and to remove the darkmode plugin if you
   don't want it
7. Deploy (on netlify, gitpages or surge, they are all free)

## ⚙️ How to run

### Pre-requisites

- NodeJS
- Ruby, Bundler

### Install

```
npm install
gem install bundler -v "$(grep -A 1 "BUNDLED WITH" Gemfile.lock | tail -n 1)"
bundler install
```

### Development

```
npm start
```

### Build

```
npm run build
```
