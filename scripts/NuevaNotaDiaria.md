<%*
const moment = tp.date.now("YYYY-MM-DD");
const dailyPath = Notas diarias 🗞️/Octubre~Diciembre 2025/🗓️Noviembre/${moment}.md;
const plantilla = "Plantillas/Diaria";

// Comprueba si la nota ya existe
if (!await app.vault.adapter.exists(dailyPath)) {
  const contenido = await tp.file.include([${plantilla}]);
  await app.vault.create(dailyPath, contenido);
  console.log("✅ Nota diaria creada:", dailyPath);
} else {
  console.log("ℹ️ La nota diaria ya existía:", dailyPath);
}
%>