<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Losowe Imię</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

<div id="imie-container">
    <h1 id="imie">Kliknij poniżej, aby zobaczyć losowe imię!</h1>
    <button onclick="losujImie()">Losuj Imię</button>
</div>

<script>
    // Lista dostępnych imion
    var imiona = ["Alina", "Michał", "Mateusz", "Nikola", "Przemek", "Sylwia", "Marek", "Renata"];

    // Funkcja do losowania i wyświetlania imienia
    function losujImie() {
        // Sprawdź, czy wszystkie imiona zostały użyte
        if (imiona.length === 0) {
            alert("Wszystkie imiona zostały użyte!");
            return;
        }

        // Losuj indeks imienia
        var indeks = Math.floor(Math.random() * imiona.length);

        // Pobierz losowe imię i usuń je z listy
        var wylosowaneImie = imiona.splice(indeks, 1)[0];

        // Wyświetl imię na stronie
        document.getElementById("imie").textContent = wylosowaneImie;
    }
</script>

</body>
</html>
