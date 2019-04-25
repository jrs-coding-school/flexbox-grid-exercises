<script>
import router from 'page'

import Start from './Start.svelte'
import FlexboxMenu from './flexbox/Menu.svelte'
import Flexbox1 from './flexbox/1.html'
import Flexbox2 from './flexbox/2.html'
import Flexbox3 from './flexbox/3.html'
import Flexbox4 from './flexbox/4.html'


let page = Start

router('/', () => page = Start)
router('/flexbox', () => page = FlexboxMenu)

router('/flexbox/1', () => page = Flexbox1)
router('/flexbox/2', () => page = Flexbox2)
router('/flexbox/3', () => page = Flexbox3)
router('/flexbox/4', () => page = Flexbox4)


router.start()

</script>

<svelte:component this={page} />
