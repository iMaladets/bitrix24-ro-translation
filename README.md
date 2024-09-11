# bitrix24-ro-translation
Traduce textul widget-ului integrat CRM BItrix24 în limba română.

## Cum îl folosiți?
Asigurați-vă că aveți instalat codul widget-ului pe site, care ar trebui să arate așa:

```javascript
(function(w, d, u) {
       var s = d.createElement('script');
       s.async = true;
       s.src = u + '?' + (Date.now() / 60000 | 0);
       var h = d.getElementsByTagName('script')[0];
       h.parentNode.insertBefore(s, h);
})(window, document, 'https://cdn-ru.bitrix24.ru/******/crm/site_button/loader_4_qd0hps.js');
```
### Activarea

Exemplu de instalare și activare

Insalați fișierul în mapa predeterminată de proiectul Dumneavoastră, ex "assets/helpers/translation/bitrixcrmwidget_ro.json"

```javascript
window.addEventListener('onBitrixLiveChat', async function(event) {
    widget = event.detail.widget;
    const res = await fetch('/assets/helpers/translation/bitrixcrmwidget_ro.json')
    if(res.ok){
      let translate = await res.json()
      widget.addLocalize(translate);
  }
}
```
