# Phone Hunting
### Hosted link: https://Dakshayini1.github.io/PhoneHunting/

### Step 1: Create a New HTML File

Create a new HTML file and save it as `index.html`. Add the following code to your HTML file:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Phone Hunting</title>
    <link
      href="https://cdn.jsdelivr.net/npm/daisyui@3.6.2/dist/full.css"
      rel="stylesheet"
      type="text/css"
    />
    <script src="https://cdn.tailwindcss.com"></script>
   
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <style>
      .body {
        font-family: "Poppins", sans-serif;
      }
    </style>
  </head>
  <body class="body">
    <nav class="flex justify-between py-10 px-20 bg-[#0d6efd0d]">
      <h2 class="text-2xl font-bold">Hot Gadgets</h2>
      <button class="btn btn-primary text-white">Sign Up</button>
    </nav>
    <header>
      <section class=" bg-[#0d6efd0d] pb-96">
        <h1 class="text-6xl font-bold text-center">Apple Iphone 13 Pro Max</h1>
        <p class="text-lg text-center my-6">
          There are many variations of passages of Lorem Ipsum available, but
          the majority <br> have suffered alteration in some form, by injected humou.
        </p>
        <div class="flex justify-center">
          <button class="btn btn-primary text-white">Buy Now</button>

        </div>
      </section>
      <section>
        <div class="grid grid-cols-3 lg:flex lg:justify-center items-end relative bottom-80 -mb-72">
          <img src="./images/pngwing 2.png" alt="">
          <img src="./images/pngwing 1.png" alt="">
          <img src="./images/pngwing 2.png" alt="">
        </div>
      </section>
      <h1 class="text-4xl text-center font-bold my-10">Search Your Phone</h1>
    </header>
    <main>
     
      <section class="flex justify-center items-center gap-2">
        <input
          id="searchField"
          type="text"
          placeholder="e.g. oppo, samsung, iphone"
          class="input input-bordered w-full max-w-xs my-5"
        />
        <button onclick="searchHandler()" class="btn btn-primary text-white">
          Search
        </button>
 
      </section>
      
      <section>
        <div class="text-center my-40 hidden" id="loading">
          <h1>Searching</h1>
          <span class="loading loading-ring loading-lg"></span>
        </div>

        <div
          id="phone-container"
          class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10 mx-8 my-5"
        ></div>
      </section>
      <div class="hiddenflex justify-center my-8" id="showALLBtn">
        <button onclick="showBtn()" class="btn btn-primary text-white">Show All</button>
      </div>

      
      <section>
        
        <dialog id="my_modal" class="modal modal-bottom sm:modal-middle">
          <form method="dialog" class="modal-box text-center">
            <div id="imgContainer" class="flex justify-center"></div>
            <h3 id="detailsPhoneName" class="font-bold text-lg mt-3"></h3>
            <h3 id="detailsBrand" class="py-4"></h3>
            <p id="detailsSpec"></p>
            <p id="releaseDate" class="my-2"></p>

            <div class="modal-action flex justify-center">
              
              <button class="btn bg-red-600 text-white">Close</button>
            </div>
          </form>
        </dialog>
      </section>
    </main>
    
    <footer class="footer footer-center p-10 bg-[#0d6efd0d] text-black mt-20 py-32">
      <div class="text-lg">
        <svg width="50" height="50" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd" clip-rule="evenodd" class="inline-block fill-current"><path d="M22.672 15.226l-2.432.811.841 2.515c.33 1.019-.209 2.127-1.23 2.456-1.15.325-2.148-.321-2.463-1.226l-.84-2.518-5.013 1.677.84 2.517c.391 1.203-.434 2.542-1.831 2.542-.88 0-1.601-.564-1.86-1.314l-.842-2.516-2.431.809c-1.135.328-2.145-.317-2.463-1.229-.329-1.018.211-2.127 1.231-2.456l2.432-.809-1.621-4.823-2.432.808c-1.355.384-2.558-.59-2.558-1.839 0-.817.509-1.582 1.327-1.846l2.433-.809-.842-2.515c-.33-1.02.211-2.129 1.232-2.458 1.02-.329 2.13.209 2.461 1.229l.842 2.515 5.011-1.677-.839-2.517c-.403-1.238.484-2.553 1.843-2.553.819 0 1.585.509 1.85 1.326l.841 2.517 2.431-.81c1.02-.33 2.131.211 2.461 1.229.332 1.018-.21 2.126-1.23 2.456l-2.433.809 1.622 4.823 2.433-.809c1.242-.401 2.557.484 2.557 1.838 0 .819-.51 1.583-1.328 1.847m-8.992-6.428l-5.01 1.675 1.619 4.828 5.011-1.674-1.62-4.829z"></path></svg>
        <p class="font-bold">
          Hot Gadgets BD <br/>Providing reliable tech items since 1992
        </p> 
        <p>Copyright © 2023 - All right reserved</p>
      </div> 
      <div>
        <div class="grid grid-flow-col gap-4">
          <a><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" class="fill-current"><path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"></path></svg></a> 
          <a><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" class="fill-current"><path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"></path></svg></a> 
          <a><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" class="fill-current"><path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"></path></svg></a>
        </div>
      </div>
    </footer>
  </body>
  
  <script src="js/index.js"></script>
</html>
```


### Step 2: Create a New js File

Create a new js file and save it as `index.js`. Add the following code to your js file:
```

let searchText='13';

function searchHandler(isShowAll){
    loading(true);
    const searchField=document.getElementById("searchField");
    searchText=searchField.value;
    loadPhone(searchText,isShowAll);
    
}
const loading= (isLoading)=>
{
    
    const loading= document.getElementById("loading");
    if(isLoading)
    {
        loading.classList.remove('hidden');
    }
    else{
        loading.classList.add('hidden');
    }

}

const loadPhone= async(searchText,isShowAll)=>{
    const res = await fetch(`https://openapi.programming-hero.com/api/phones?search=${searchText}`);
    const data =await res.json();
    const phones = data.data;
    displayPhones(phones,isShowAll);
    
}
loadPhone(searchText);
const displayPhones = (phones,isShowAll)=>{
    
    const phoneContainer= document.getElementById("phone-container");
    phoneContainer.textContent='';
    
    const showAll= document.getElementById("showALLBtn");
    if(phones.length>12 && !isShowAll)
    {
        showAll.classList.remove('hidden');
        
        
    }
    else
    {
        showAll.classList.add('hidden');
    }
    
    if(!isShowAll)
    {
        phones=phones.slice(0,12);
    }
    
    phones.forEach(phone => {
       
        const phoneCard=document.createElement('div');
        phoneCard.classList=`card bg-base-100 shadow-xl p-5`;
        phoneCard.innerHTML=`
        <figure class="px-10 pt-10">
                      <img src="${phone.image}" alt="phone" class="rounded-xl" />
                    </figure>
                    <div class="card-body items-center text-center">
                      <h2 class="card-title">${phone.phone_name}</h2>
                      <p>There are many variations of passages of available, but the majority have suffered</p>
                      <div class="card-actions">
                        <button onclick="showDetailsHandler('${phone.slug}')" class="btn btn-primary text-white">Show Details</button>
                      </div>
                    </div>

        `;
        phoneContainer.appendChild(phoneCard);
        
    });
    
    loading(false);
    
}


function showBtn()
{
   searchHandler(true);
}

const showDetailsHandler = async (id)=>{
    
    const res= await fetch(`https://openapi.programming-hero.com/api/phone/${id}`);
    const data=await res.json();
    
    const phone=data.data;
    showPhoneDetails(phone);
    
}
const showPhoneDetails=(details)=>{
    my_modal.showModal();
    const modelName= document.getElementById('detailsPhoneName');
    const brandName= document.getElementById('detailsBrand');
    const detailsSpec= document.getElementById('detailsSpec');
    const releaseDate= document.getElementById('releaseDate');
    const imageDiv= document.getElementById('imgContainer');

    imageDiv.innerHTML=`<img src="${details.image}" alt="">`;
    modelName.innerText=details.name;
    brandName.innerText=`Brand: ${details.brand}`;
    const features=details.mainFeatures;
    
    console.log(details.image);
    let string="";
    for (const key in features) {

        
        string=string+`${key}: ${features[key]} \n`;

    }
    detailsSpec.innerText=string;
    releaseDate.innerText=`${details.releaseDate}`;
    
}


```
