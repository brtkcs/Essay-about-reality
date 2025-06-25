
# Munkafolyamat – Branch és Verziókezelés

Ez a dokumentum összefoglalja az `about-reality` disszertációs projekt verziókövetési rendszerét.

---

## Ágak (branches)

### `main`
A fő ág. Itt található a legfrissebb, stabil munkaállapot. Minden jelentős fejlesztés itt kerül először összefoglalásra.

### `draft`
Szabad kísérletezés, ötletelés, gyors iterációk helye. Itt lehet „garázdálkodni” – nem szükséges teljes koherencia vagy formalitás.

### `public`
A publikálható, olvasásra szánt verzió. Ebből készül a HackMD-s közzététel, később a beadandó is. Csak ellenőrzött, rendezett részek kerülnek ide.

---

## Verziózás (tags)

- A verziók `v0.xx` formátumban kerülnek kijelölésre.
- **`v0.01`**: az első teljes mesterverzió, minden eddigi fájl integrálva.
- Minden jelentősebb publikációs lépés új verziót kap.

---

## Munkamenet (workflow)

1. **Fejlesztés** – `draft` ágban történik
2. **Stabilizálás** – `draft` → `main` beolvasztás
3. **Publikálás** – `main` → `public` válogatott beolvasztás
4. **Verziózárás** – `tag` kiadása, pl. `v0.02`

---

## Példa Git parancsokra

```bash
# új ág indítása kísérletezéshez
git checkout -b draft

# munka visszaváltása a fő ágra
git checkout main

# draft beolvasztása a main-be
git merge draft

# publikálható verzió frissítése
git checkout public
git merge main

# új verzió kijelölése
git tag v0.01
```

---

📝 **Megjegyzés**: a `draft` ágban mindenféle kísérlet helyet kaphat – akár félkész ötletek, nem teljes szövegek is. Ez a kreatív tér, itt nincs jó vagy rossz irány – csak építkezés.
