<script>
  import avatar00 from "../assets/avatar/user00.png";
  import avatar01 from "../assets/avatar/user01.png";
  import avatar02 from "../assets/avatar/user02.png";
  let users = [
    {
      id: 1,
      image: avatar00,
      name: "Max",
      email: "Max@max.xyz",
    },
    {
      id: 2,
      image: avatar01,
      name: "Oh",
      email: "Oh@max.xyz",
    },
    {
      id: 3,
      image: avatar02,
      name: "Ken",
      email: "Ken@max.xyz",
    },
  ];

  const getUsers = () => {
    return users;
  };
</script>

<div>
  <h1 class="text-2xl text-center mt-10">List of Users</h1>
  {#each getUsers() as { name, image, email,id }, i(id)}
    <div class="flex m-5 bg-white border p-2 rounded-2xl shadow-md hover:shadow-lg cursor-pointer items-center">
      <p class="w-10">{i + 1}</p>
      <img class="rounded-full w-14 h-14 mx-4" src={image} alt="" />
      <p class="mx-4 w-20">{name}</p>
      <p class="mx-4 w-20">{email}</p>
    </div>
  {:else}
    <p>No user found.</p>
  {/each}
</div>
