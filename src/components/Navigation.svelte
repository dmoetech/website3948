<script>
    import CustomContainer from "../components/Container.svelte";

    let navbarOpen = false;

    function toggleNavbar() {
        navbarOpen = !navbarOpen;
    }
</script>

<!-- <div class="overflow-x-hidden sticky top-0 z-50"> -->
<div class="relative overflow-hidden">
    <CustomContainer customClass="relative bg-blue-600 z-50">
        <div class="border-b border-gray-400 py-2 flex relative z-10 flex-col md:flex-row">
            <a class="text-gray-300 flex items-center hover:text-white cursor-pointer my-3 md:my-0" href="tel:00491712198934">
                <svg viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5 mr-2">
                    <path
                        d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z">
                    </path>
                </svg>
                <span class="block">0171 2198934</span>
            </a>
            <a class="text-gray-300 flex items-center hover:text-white cursor-pointer md:ml-auto mb-3 md:mb-0"
                href="mailto:kontakt@id-gebaeudemanagement.de?subject=Anfrage">
                <svg viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5 mr-2">
                    <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path>
                    <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path>
                </svg>
                <span class="block">kontakt@id-gebaeudemanagement.de</span>
            </a>
        </div>
        <div class="absolute bg-blue-500 bottom-0 right-0 w-full h-800 transform origin-bottom-right rotate-75 z-0 {navbarOpen ? 'bg-blue-600' : ''}"
            style="--transform-translate-y: 80px">
        </div>
        <div class="absolute bg-blue-500 bottom-0 left-0 w-full h-800 transform origin-bottom-left -rotate-75 z-0 {navbarOpen ? 'bg-blue-600' : ''}"
            style="--transform-translate-y: 80px">
        </div>
        <div class="absolute bg-blue-600 bottom-0 right-0 w-full h-800 transform origin-bottom-right rotate-45 z-0"
            style="--transform-translate-y: 80px">
        </div>
        <div class="absolute bg-blue-600 bottom-0 left-0 w-full h-800 transform origin-bottom-left -rotate-45 z-0"
            style="--transform-translate-y: 80px">
        </div>
    </CustomContainer>
</div>
<nav class="sticky top-0 outline-none z-40">
    <div class="overflow-x-hidden">
        <div class="">
            <CustomContainer customClass="bg-blue-600 relative">
                <div class="flex items-center justify-between flex-wrap py-0 relative z-50">
                    <div class="flex items-center flex-shrink-0 text-white mr-6 h-20">
                        <!-- <svg class="fill-current h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54"
                    xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z" />
                </svg> -->
                        <!-- <img class="w-auto h-20 mr-3 md:hidden" src="logo.jpg" alt="Firmenlogo"> -->
                        <span class="font-semibold text-lg md:text-xl tracking-tight">I.D. Gebäudemanagement</span>
                    </div>
                    <div class="block lg:hidden">
                        <button on:click={toggleNavbar}
                            class="flex items-center px-4 py-3 border rounded text-gray-400 border-gray-400 hover:text-white hover:border-white focus:outline-none">
                            <svg class="fill-current h-4 w-4" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                                <title>Menu</title>
                                <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
                            </svg>
                        </button>
                    </div>
                    <div class="w-full flex-grow lg:flex lg:items-center lg:w-auto { navbarOpen ? 'block' : 'hidden' }">
                        <div class="text-sm lg:flex-grow lg:text-right">
                            <a href="." on:click="{() => {navbarOpen = false}}"
                                class="block mt-4 lg:inline-block lg:mt-0 text-gray-100 text-lg hover:border-gray-200 border border-transparent rounded px-2 lg:px-1 p-1 hover:text-white lg:mr-4 focus:outline-none">
                                Startseite
                            </a>
                            <a href="leistungen/" on:click="{() => {navbarOpen = false}}"
                                class="block mt-4 lg:inline-block lg:mt-0 text-gray-100 text-lg hover:border-gray-200 border border-transparent rounded px-2 lg:px-1 p-1 hover:text-white lg:mr-4 focus:outline-none">
                                Leistungen
                            </a>
                            <a href="anfrage/" on:click="{() => {navbarOpen = false}}"
                                class="block mt-4 lg:inline-block lg:mt-0 text-gray-100 text-lg hover:border-gray-200 border border-transparent rounded px-2 lg:px-1 p-1 hover:text-white lg:mr-4 focus:outline-none">
                                Anfrage
                            </a>
                            <a href="kontakt/" on:click="{() => {navbarOpen = false}}"
                                class="block mt-4 mb-4 lg:mb-0 lg:inline-block lg:mt-0 text-gray-100 text-lg hover:border-gray-200 border border-transparent rounded px-2 lg:px-1 p-1 hover:text-white lg:-mr-1 focus:outline-none">
                                Kontakt
                            </a>
                        </div>
                    </div>
                </div>
                <div
                    class="absolute bg-blue-500 bottom-0 left-0 w-full h-800 transform origin-bottom-left -rotate-75 z-0">
                </div>
                <div
                    class="absolute bg-blue-500 bottom-0 right-0 w-full h-800 transform origin-bottom-right rotate-75 z-0">
                </div>
                <div
                    class="absolute bg-blue-600 bottom-0 left-0 w-full h-800 transform origin-bottom-left -rotate-45 z-0">
                </div>
                <div
                    class="absolute bg-blue-600 bottom-0 right-0 w-full h-800 transform origin-bottom-right rotate-45 z-0">
                </div>
            </CustomContainer>
        </div>
    </div>
</nav>
<!-- <div class="absolute bg-white top-0 left-0 w-64 h-64 rotate-45 transform origin-top-left"></div>
    <div class="absolute bg-white top-0 right-0 w-64 h-64 -rotate-45 transform origin-top-right"></div> -->
<!-- </div> -->