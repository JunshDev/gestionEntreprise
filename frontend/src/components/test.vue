<template>
    <div>
        <nav class=" border-gray-200 px-2 sm:px-4 py-2.5   ">
            <div
                class="container bg-white p-4 flex flex-wrap justify-around items-center mx-auto fixed z-50 top-0 w-full left-0 shadow-2xl">
                <a href="/">
                    <img src="../assets/images/logo1.svg" class="mr-3 h-6 sm:h-9">
                </a>
                <button data-collapse-toggle="mobile-menu" type="button"
                    class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
                    aria-controls="mobile-menu" aria-expanded="false">
                    <span class="sr-only">Open main menu</span>
                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd"
                            d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                            clip-rule="evenodd"></path>
                    </svg>
                    <svg class="hidden w-6 h-6" fill="currentColor" viewBox="0 0 20 20"
                        xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd"
                            d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                            clip-rule="evenodd"></path>
                    </svg>
                </button>
                <div class="hidden w-full md:block md:w-auto" id="mobile-menu">
                    <ul class="flex flex-col mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium">
                        <li>
                            <a href="/"
                                class="block py-2 pr-4 pl-3 text-white bg-primary rounded md:bg-transparent md:text-primary md:p-0 text-lg font-normal dark:text-white"
                                aria-current="page">Home</a>
                        </li>
                        <!-- <li>
                            <a href="#about"
                                class="block py-2 pr-4 pl-3 text-secondary border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-primary md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white text-lg font-normal md:dark:hover:bg-transparent dark:border-gray-700">About
                                Us</a>
                        </li> -->
                        <li>
                            <a href="/products"
                                class="block py-2 pr-4 pl-3 text-secondary border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 text-lg font-normal md:hover:text-primary md:p-0 ">Abouts US</a>
                        </li>
                        <!-- <li>
                            <a href="#services"
                                class="block py-2 pr-4 pl-3 text-secondary border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 text-lg font-normal md:hover:text-primary md:p-0 ">Services</a>
                        </li> -->
                        <li>

                            <a href="/Contact"
                                class="block py-2 pr-4 pl-3 text-secondary hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:text-secondary md:p-0 text-lg font-normal dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Contact
                                Us</a>
                        </li>
                        <li>
                            <div v-if="id">
                                <a href="/admin"
                                    class="block py-2 pr-4 pl-3 text-secondary hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:text-secondary md:p-0 text-lg font-normal dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Dashboard</a>
                            </div>
                            <div v-else>
                                <a href="/login"
                                    class=" py-2 pr-4 pl-3 text-secondary hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:text-secondary md:p-0 text-lg font-normal dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Login</a>
                            </div>
                        </li>
                        <li>

                            <a href="/signup" class=" w-20  border-4 border-secondary  rounded hover:text-primary hover:bg-gray-50 md:hover:bg-transparent md:text-white md:bg-secondary md:te md:border-2 md:p-2 text-lg font-normal dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text-primary" >  Sign Up </a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>
<script>
export default {
    setup() {

        let id = $cookies.get("id") ? true : false;
        console.log(id);
        console.log("if true login not in navbar");

    }
}
</script>