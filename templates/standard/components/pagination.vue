pagination
["view", "pages", "currentPage"]
<div class="display-inline">
    <template v-if='pages.length > 1'>
        <span id="paging" class="pagination">
            <button class="float-none" v-bind:onclick="'pagination.loadPrevPage(' + view +')'"><<</button>

            <span id="page{{page.index}}" v-for="page in pages" class="margin-left-two-px">
               <button v-bind:class="currentPage == page.index ? 'paginationActive' : 'paginationInactive'"
                        v-bind:onclick="'pagination.loadPage(' + view +', '+page.index+')'">
                    {{page.index}}
               </button>
            </span>

            <button class="float-none" v-bind:onclick="'pagination.loadNextPage(' + view +')'">>></button>
        </span>
    </template>
</div>