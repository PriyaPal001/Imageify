<script lang="ts">
    import * as Card from "$lib/components/ui/card/index.js";
    import * as Carousel from "$lib/components/ui/carousel/index.js";

    let items = [
		{ img: 'https://i.pinimg.com/736x/26/86/bd/2686bd85258ce9599f33b2c9895508c7.jpg' },
		{ img: 'https://i.pinimg.com/736x/05/0a/1d/050a1db06ac622f1ab48ba02405cf378.jpg' },
		{
			img: 'https://i.pinimg.com/736x/b1/64/b8/b164b8db6056d217c5ceaf9798a123a3.jpg'
		},
		{
			img: 'https://i.pinimg.com/736x/81/49/34/814934c68bb9bc9bf222d3032ad0f280.jpg'
		},
		{
			img: 'https://i.pinimg.com/736x/38/09/d0/3809d01cdc1bcc2af3bc6fc530858bf5.jpg'
		}
    ]
   </script>
    
   <Carousel.Root
    opts={{
     align: "start"
    }}
    orientation="vertical"
    class="w-full max-w-xs"
   >
    <Carousel.Content class="-mt-1 h-[200px]">
     {#each items as i }
      <Carousel.Item class="pt-1 md:basis-1/2">
       <div class="p-1">
        <Card.Root>
         <Card.Content class="flex items-center justify-center p-6">
          <img src={i.img} alt="">
         </Card.Content>
        </Card.Root>
       </div>
      </Carousel.Item>
     {/each}
    </Carousel.Content>
    <Carousel.Previous />
    <Carousel.Next />
   </Carousel.Root>