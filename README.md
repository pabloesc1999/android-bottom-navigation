<img width="210" height="462" alt="image" src="https://github.com/user-attachments/assets/68ccc18a-5fd5-4b31-9c90-f48b0bcfce57" />
<img width="214" height="462" alt="image" src="https://github.com/user-attachments/assets/e5d6aa79-3346-4f48-9c95-9088c0e901f7" />
<img width="217" height="461" alt="image" src="https://github.com/user-attachments/assets/53952705-af7c-49f0-9747-96a92801910c" />







# 🧭 Android Bottom Navigation (One Activity, Zero Drama)

So you want bottom navigation. Three screens. One Activity. No chaos. You've come to the right repo.

![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android&logoColor=white)
![Language](https://img.shields.io/badge/language-Kotlin-7F52FF?logo=kotlin&logoColor=white)
![Architecture](https://img.shields.io/badge/architecture-1%20Activity%2C%203%20Fragments-orange)
![Vibes](https://img.shields.io/badge/vibes-immaculate-ff69b4)

---

## 🎭 What is this, actually

Three screens. One Activity holding all of them hostage, as God and Google intended. Tap an icon at the bottom, the screen changes, nobody panics, nothing gets destroyed and recreated fifty times for no reason.

- 🏠 **Home** — the screen that greets you like it didn't just get swapped in by a `NavController`
- 🔍 **Search** — has a search bar. It doesn't *search* anything yet. It's aspirational.
- 🔖 **Bookmark** — exists. Judges you for not bookmarking anything.

---

## 🧠 Why no extra Activities?

Because spinning up a new Activity for every screen is how you end up with 14 `Intent`s, 6 memory leaks, and a prayer. One Activity, three Fragments, one `NavHostFragment` doing the actual work while `MainActivity` just sits there looking responsible.

---

## 🛠️ Built With

- **Kotlin** — obviously
- **Navigation Component** — `NavGraph`, `NavHostFragment`, `NavController`, the whole family
- **Fragments** — three of them, each minding its own business
- **BottomNavigationView** — with real icons, not sad little text labels
- **ConstraintLayout** — because `LinearLayout` is for cowards

---

## 🚀 Running This Thing

```bash
git clone https://github.com/pabloesc1999/android-bottom-navigation.git
```

Open in Android Studio, let Gradle do its Gradle things, hit run. If it doesn't build, check your package names before you check your sanity — that's usually where the bug is hiding.

---

## 📂 The Anatomy

app/src/main/
├── java/com/example/navgraphfragments/
│ ├── MainActivity.kt # The one true Activity
│ ├── HomeFragment.kt # Screen 1
│ ├── SearchFragment.kt # Screen 2 (searches nothing, promises everything)
│ └── BookmarkFragment.kt # Screen 3
└── res/
├── navigation/
│ └── nav_graph.xml # The actual brain of this operation
├── menu/
│ └── bottom_nav_menu.xml
└── layout/
├── activity_main.xml
├── fragment_home.xml
├── fragment_search.xml
└── fragment_bookmark.xml


---

## ⚠️ Known Quirks

- The search bar is decorative. It will not search. It will judge you for trying.
- If your icons look weird in the vector asset picker, make sure you're on **Filled**, not whatever cursed "Material Symbols" variant it defaults to.
- "Elements not declared" warning on the menu XML? Ignore it. It's lying.

---

## 🗺️ Roadmap (lol)

- [ ] Make the search bar actually search
- [ ] Add a real bookmark list instead of a vibe
- [ ] Dark mode that doesn't look like an afterthought

---

## 👤 Author

**Shaban Saeed**
[GitHub](https://github.com/pabloesc1999) — learning Android one slightly over-engineered side project at a time.

---

## 📄 License

MIT. Take it, fork it, just don't blame me when the search bar doesn't search.
