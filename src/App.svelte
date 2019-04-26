<script>
import router from 'page'

import Start from './Start.svelte'
import FlexboxMenu from './flexbox/Menu.svelte'
import Flexbox1 from './flexbox/1.html'
import Flexbox2 from './flexbox/2.html'
import Flexbox3 from './flexbox/3.html'
import Flexbox4 from './flexbox/4.html'

import GridMenu from './cssgrid/Menu.svelte'
import Grid1 from './cssgrid/1.html'
import Grid2 from './cssgrid/2.html'
import Grid3 from './cssgrid/3.html'



let page = Start

router('/', () => page = Start)
router('/flexbox', () => page = FlexboxMenu)

router('/flexbox/1', () => page = Flexbox1)
router('/flexbox/2', () => page = Flexbox2)
router('/flexbox/3', () => page = Flexbox3)
router('/flexbox/4', () => page = Flexbox4)

router('/cssgrid', () => page = GridMenu)

router('/cssgrid/1', () => page = Grid1)
router('/cssgrid/2', () => page = Grid2)
router('/cssgrid/3', () => page = Grid3)


router.start()

</script>

<svelte:component this={page} />
