<script>
  import Step from "./Step.svelte";

  let steps = [
    { name: "Vernam Cipher/One Time Pad", icon: "fa-solid fa-lock" },
    { name: "Secure Enhanced Geolocking", icon: "fa-solid fa-earth-americas" },
    { name: "AdminOps Script", icon: "fa-solid fa-people-roof" },
  ];

  let benefits = [
    {
      name: "a self-taught ethical hacker",
      description: `I taught myself how to code from free online resources
                      starting with Java. Once I started getting comfortable with various data structures and algorithms, I found my calling- Information Security.
                      I've been hooked on expanding ever since, and do not plan on stopping.`,
    },
    {
      name: "an avid pen-tester",
      description: `I love seeking out bugs and vulnerabilities. It has become a hobby of mine and serves to teach more and more
                      every time. Pretty safe to say, I love bugs. Hate when they bite though.`,
    },
    {
      name: "an excellent communicator",
      description: `Communication is key and it is a paramount value of mine. I believe in transparency and constructive
                      communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.`,
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Harshit</span> Chauhan
        <br />An Aspiring VAPT
        <span class="poppins text-violet-400">Engineer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite skills</span> include Ethical
        Hacking and Penetration Testing. I
        <span class="text-violet-400">love</span> to work in Java and Debian-based
        Linux Distributions!
      </p>
      <a
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg
            md:text-xl poppins relative overflow-hidden px-6 py-3 group
            rounded-full bg-white text-slate-950 cursor-pointer"
        href="https://drive.google.com/file/d/1VlA72w-tMCn_e5T6R6EjEdP6E0efb69u/view?usp=sharing"
        target="_blank"
      >
        <div
          class="absolute top-0 right-full w-full h-full
                    bg-violet-400 opacity-20 group-hover:translate-x-full z-0
                    duration-200"
        />
        <h4 class="relative z-9">My Resume &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <!-- svelte-ignore a11y-img-redundant-alt -->
      <img
        src={"images/profile.png"}
        alt="Profile image"
        class="object-cover z-[2] max-h-[70vh]"
      />
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-w text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavours.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to <span class="poppins text-violet-400">see</span>
        my work?
      </h3>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          The Secure Messaging System is an advanced encryption project designed to ensure the utmost security for confidential messages. The encryption technique employed is the Vernam cipher, commonly known as the<strong class="text-violet-400">
            Vernam Cipher/One Time Pad. </strong
          > This encryption method transforms plaintext messages into ciphertext by utilizing randomly generated keys, ensuring unparalleled security. Demonstrated in Jupyter Notebook in python, libraries used were secrets and string
          
        </p>
      </Step>

      <Step step={steps[1]}>
        <p>
          This project aims at improving the geolocking technique by providing
          tools for specifying and enforcing the designated reception
          geolocation area and encrypting data with web cryptography standard.
          Location is chosen to restrict access since the area can now be
          specified uniquely and be verified with enough precision. Tools used
          were <strong class="text-violet-400">
            JavaScript and server side PHP scripts with Web Crypto API and Maria
            DB
          </strong>
        </p>
      </Step>

      <Step step={steps[2]}>
        <p>
          AdminOps Shell Script streamlines Linux system administration by
          offering a user-friendly interface for essential tasks with verbose mode toggling. From adding
          and deleting users to generating secure passwords and managing account
          security, this script ensures a seamless and secure administrative
          experience. Elevate your system management capabilities with AdminOps
          Shell Script – where simplicity meets efficiency in user and account
          management. Tools used were:
          <strong class="text-violet-400">
            Vim as a text Editor and Bash.</strong
          >
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3
        before:h-1.5 before:bg-violet-700
        after:absolute after:bottom-0 after:right-0 after:w-2/3
        after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span> me.
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am . . .
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
      <div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
          The <span class="text-violet-400 poppins">Complete </span>Package.
        </h5>
        <div
          class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
          <table class="bg-white text-slate-700 rounded text-center">
            <thead class="border-b border-solid border-slate-200">
              <tr>
                <th class="whitespace-nowrap p-2 px-4">Attribute</th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8"
                  >Me</th
                >
              </tr>
            </thead>
            <tbody>
              <tr>
                <td
                  class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                  >Dedication</td
                >
                <td><i class="fa-solid fa-check text-slate-500" /></td>
                <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-green-500" /></td>
              </tr>
              <tr>
                <td
                  class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                  >Critical Thinking</td
                >
                <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-green-500" /></td>
              </tr>
              <tr>
                <td
                  class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                  >Interpersonal Skills</td
                >
                <td><i class="fa-solid fa-check text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-green-500" /></td>
              </tr>
              <tr>
                <td
                  class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                  >Hacking Abiliity</td
                >
                <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                <td><i class="fa-solid fa-check text-green-500" /></td>
              </tr>
            </tbody>
          </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
          <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why not invest?</p>
      </div>
    </div>
  </section>
</main>
