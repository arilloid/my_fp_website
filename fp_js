window.onload = function() {
    var today = new Date();
    var date = document.createTextNode(today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate());
    document.getElementById("date").appendChild(date);
   
    const form = document.getElementById("formid");
    const postalCodeEl = document.getElementById("postal-code");
    const isPostalValid = (postal) => {
        const postalRegex = /^[A-Za-z]\d[A-Za-z][ -]?\d[A-Za-z]\d$/;
        return postalRegex.test(postal);
    }
    
    form.addEventListener('submit', (e) => {
        var postalCode = postalCodeEl.value.trim();
        if (!isPostalValid(postalCode)) {
            e.preventDefault();
            postalCodeEl.setCustomValidity('Please enter a valid postal code.');
        } else {
            postalCodeEl.setCustomValidity('');
        }
        postalCodeEl.reportValidity();
    })

    //displaying the hourly rate
    const rate = document.getElementById("rate");
    document.getElementById("question").addEventListener("change", () => {
        rate.style.display = "none";
      }); 
    document.getElementById("comment").addEventListener("change", () => {
        rate.style.display = "none";
    });
    document.getElementById("hiring").addEventListener("change", () => {
        rate.style.display = "grid";
    });
}
