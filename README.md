# Otto – chatbot me Claude

## Si ta bësh deploy (falas, pa instaluar gjë)

1. **Merr API key nga Claude**
   - Hyr te https://console.anthropic.com
   - Shto kredit te *Billing* (minimumi 5$)
   - Te *API Keys* shtyp **Create Key** dhe kopjoje (fillon me `sk-ant-...`)

2. **Ngarkoje kodin në GitHub**
   - Bëj llogari te https://github.com
   - **New repository** → emri `otto` → **Create**
   - **uploading an existing file** → tërhiq brenda të gjithë skedarët e folderit `otto`
     (`index.html`, `package.json`, `README.md` dhe folderin `api`) → **Commit changes**

3. **Deploy në Vercel**
   - Hyr te https://vercel.com me llogarinë GitHub
   - **Add New → Project** → zgjidh `otto` → **Import**
   - Hape **Environment Variables** dhe shto:
     - Name: `ANTHROPIC_API_KEY`
     - Value: key-i që kopjove te hapi 1
   - Shtyp **Deploy**

4. Pas ~1 minute merr një link si `https://otto-xxxx.vercel.app`. Hape dhe fol me Otto.

## Ndryshime
- Si sillet Otto: ndrysho tekstin `SYSTEM` te `api/chat.js`
- Modeli: `claude-opus-5-5` (më i fuqishmi). Për më lirë vendos `claude-sonnet-5-5` ose `claude-haiku-5-5`.

**Mos e vendos kurrë API key-in brenda kodit ose në GitHub.** Vendose vetëm në Vercel.
