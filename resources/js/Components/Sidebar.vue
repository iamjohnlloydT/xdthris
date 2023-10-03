<template>
    <aside class="h-screen w-full border-r-2">
        <div class="bg-red-2 flex items-center justify-center py-4 px-4">
            <img src="../../css/assets/xdt-logo.png" class="w-1/2" />
        </div>
        <hr />

        <!--Parent-->
        <div class="px-4 w-full">
            <ul class="space-y-5 mt-8 font-medium text-md text-[#000e31]">
                <div class="space-x-2 flex items-center">
                    <UserCircleIcon class="w-6 h-6" />
                    <span>{{ $page.props.auth.user.name }}</span>
                </div>
            </ul>
            <ul class="space-y-5 mt-8 font-medium text-md text-[#000e31]">
                <span>Menu</span>
            </ul>
            <ul class="space-y-5 p-5 font-medium text-[#000e31] text-sm">
                <li>
                    <Link
                        class="h-fit p-2 flex items-center space-x-2 hover:bg-[#E9E9E9] rounded-xl"
                    >
                        <ChartPieIcon class="w-6 h-6" />
                        <span>Dashboard</span>
                    </Link>
                </li>
                <li>
                    <Link

                        class="h-fit p-2 flex items-center space-x-2 hover:bg-[#E9E9E9] rounded-xl"
                    >
                        <UserGroupIcon class="w-6 h-6" />
                        <span>Employee</span>
                    </Link>
                </li>
                <li>
                    <Link
                        class="h-fit p-2 flex items-center space-x-2 hover:bg-[#E9E9E9] rounded-xl"
                    >
                        <CalendarDaysIcon class="w-6 h-6" />
                        <span>Attendance</span>
                    </Link>
                </li>
                <li>
                    <Link
                        class="h-fit p-2 flex items-center space-x-2 hover:bg-[#E9E9E9] rounded-xl"
                    >
                        <BriefcaseIcon class="w-6 h-6" />
                        <span>Leave</span>
                    </Link>
                </li>
            </ul>
            <ul class="space-y-5 mt-8 font-medium text-md text-[#000e31]">
              <div class="flex">
                <Link :href="route('logout')" method="post" as="button">
                  <ArrowRightOnRectangleIcon class="w-6 h-6"/>
                  <span>Logout</span>
                </Link>
              </div>
            </ul>
        </div>
    </aside>
</template>

<script setup>
import { ref } from "vue";
import {
    ChartPieIcon,
    UserGroupIcon,
    CalendarDaysIcon,
    BriefcaseIcon,
    UserCircleIcon,
    ArrowRightOnRectangleIcon,
} from "@heroicons/vue/24/solid";
import { Link } from "@inertiajs/vue3";
</script>
