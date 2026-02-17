// ✅ 1) Zalepi svoje linkove ovde:

// Google Forms:
// (A) forma za konsultacije
const FORM_CONSULT_URL = "PASTE_GOOGLE_FORM_CONSULT_URL_HERE";
// (B) forma za tretman
const FORM_TREATMENT_URL = "PASTE_GOOGLE_FORM_TREATMENT_URL_HERE";

// Google Calendar (opciono – samo link za pregled)
const GOOGLE_CALENDAR_URL = "PASTE_GOOGLE_CALENDAR_URL_HERE";

// Google Maps:
// Embed link (za iframe) – mora biti "embed" format
const GOOGLE_MAPS_EMBED_URL = "PASTE_GOOGLE_MAPS_EMBED_URL_HERE";
// Normal link (otvara mapu u Google Maps aplikaciji / browseru)
const GOOGLE_MAPS_LINK_URL = "PASTE_GOOGLE_MAPS_LINK_URL_HERE";

// Kontakt (dodaš kasnije)
const EMAIL_ADDRESS = "your@email.com";
const PHONE_NUMBER = "+381600000000"; // format za tel: link

function setLinks() {
  // Booking buttons
  const consultBtn = document.getElementById("btnConsult");
  const treatBtn = document.getElementById("btnTreatment");
  if (consultBtn) consultBtn.href = FORM_CONSULT_URL;
  if (treatBtn) treatBtn.href = FORM_TREATMENT_URL;

  // Calendar link
  const cal = document.getElementById("calendarLink");
  if (cal) cal.href = GOOGLE_CALENDAR_URL;

  // Map iframe + map link
  const mapFrame = document.getElementById("mapFrame");
  const mapLink = document.getElementById("mapLink");
  if (mapFrame) mapFrame.src = GOOGLE_MAPS_EMBED_URL;
  if (mapLink) mapLink.href = GOOGLE_MAPS_LINK_URL;

  // Contact
  const emailLink = document.getElementById("emailLink");
  const phoneLink = document.getElementById("phoneLink");
  if (emailLink) emailLink.href = `mailto:${EMAIL_ADDRESS}`;
  if (phoneLink) phoneLink.href = `tel:${PHONE_NUMBER}`;
}

function setYear() {
  const y = document.getElementById("year");
  if (y) y.textContent = new Date().getFullYear();
}

setLinks();
setYear();
